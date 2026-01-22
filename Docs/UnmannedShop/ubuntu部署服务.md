# 部署hub服务

### 使用管理员用户sudo su
sudo su 输入管理员登陆密码 进入管理员命令行

### 将部署文件拷贝到服务器上
### 注意xftp没权限直接拷贝到root目录，之恶能拷贝到用户的目录下
cd /home/{用户}
cd到/opt目录下执行
mkdir front
mkdir backend
mv /home/{用户}/publish.zip ./backend
mv /home/{用户}/dist.zip ./front
cd /opt/front
mkdir conf
# 复制下面的配置到conf目录下
vim default.conf
```
server {
    listen 80;
    listen [::]:80;
    server_name localhost;
    ignore_invalid_headers off;


    location / {
        root /usr/share/nginx/html;
        index index.html index.htm;
        proxy_set_header Abp.TenantId $http_abp_tenantid;
        # CORS headers
        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
        add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization,Abp.TenantId' always;
    }

    location /api {
        # Proxy settings
        proxy_pass http://192.168.18.7:8080/api;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'keep-alive';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;

        # Pass the Abp.TenantId from the client to the backend
        proxy_set_header Abp.TenantId $http_abp_tenantid;

        # CORS headers
        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
        add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization,Abp.TenantId' always;

        # Handle OPTIONS requests for /api
        if ($request_method = 'OPTIONS') {
            add_header 'Access-Control-Allow-Origin' '*' always;
            add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
            add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization,Abp.TenantId' always;
            add_header 'Access-Control-Max-Age' 1728000;
            add_header 'Content-Type' 'text/plain charset=UTF-8';
            add_header 'Content-Length' 0;
            return 204;
        }
    }

    location /sms {
        # Proxy settings
        proxy_pass http://192.168.18.9/sms;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;

        # CORS headers are sent along with requests to /api
        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
        add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization' always;

        # Handle OPTIONS requests for /api
        if ($request_method = 'OPTIONS') {
            add_header 'Access-Control-Allow-Origin' '*' always;
            add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
            add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization' always;
            add_header 'Access-Control-Max-Age' 1728000;
            add_header 'Content-Type' 'text/plain charset=UTF-8';
            add_header 'Content-Length' 0;
            return 204;
        }
    }

    location /AbpUserConfiguration/GetAll {
        # Proxy settings
        proxy_pass http://192.168.18.7:8080/AbpUserConfiguration/GetAll;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'keep-alive';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;

        # Pass the Abp.TenantId from the client to the backend
        proxy_set_header Abp.TenantId $http_abp_tenantid;

        # CORS headers
        add_header 'Access-Control-Allow-Origin' '*' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
        add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization,Abp.TenantId' always;

        # Handle OPTIONS requests for /AbpUserConfiguration/GetAll
        if ($request_method = 'OPTIONS') {
            add_header 'Access-Control-Allow-Origin' '*' always;
            add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS, PUT, DELETE, PATCH' always;
            add_header 'Access-Control-Allow-Headers' 'DNT,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,Range,Authorization,Abp.TenantId' always;
            add_header 'Access-Control-Max-Age' 1728000;
            add_header 'Content-Type' 'text/plain charset=UTF-8';
            add_header 'Content-Length' 0;
            return 204;
        }
    }

    # Error pages
    error_page 500 502 503 504 /50x.html;
    location = /50x.html {
        root /usr/share/nginx/html;
    }
}

```

### 上面涉及到ip的地方要改成对应的后台的ip跟端口
### 加压前后端打包
unzip publish.zip
unzip dist.zip

### 拉公司的阿里云镜像
docker login --username=qule@1120777826858507 registry.cn-shanghai.aliyuncs.com
密码1qaz@WSX
### 执行下面代码运行程序
docker run -d --restart always --ulimit core=0 -p 8080:8080 -p 9123:9123 -v /opt/backend/publish:/app -u $(id -u):$(id -g) -e TZ=Asia/Shanghai registry.cn-shanghai.aliyuncs.com/troncellapi/sensinghub:v3
docker run -d --restart always -v /opt/front/conf:/etc/nginx/conf.d -v /opt/front/dist:/usr/share/nginx/html -p 80:80 nginx:1.21

### 修改后端配置文件
cd /opt/backend/publish/
vim appsettings.json
```
{
  "SafeIpList": "127.0.0.1;180.114.161.134;101.132.36.100;::1",
  "ConnectionStrings": {
    //"Default": "Data Source=localhost;Initial Catalog=SensingStore.Hub;Integrated Security=False;user=sa;password=1!troncell!1;MultipleActiveResultSets=true;"
    //"Default": "server=127.0.0.1;userid=root;pwd=mypassword;port=3306;database=SensingHub;sslmode=none;AllowPublicKeyRetrieval=true",
    //"Default": "server=172.17.0.1;userid=root;pwd=1!Troncell!1;port=3306;database=SensingHub;sslmode=none;"
    //        "Default": "server=192.168.2.11;userid=root;pwd=123456;port=30306;database=sensinghub-panshi;sslmode=none;AllowPublicKeyRetrieval=true"
    //    "Default": "server=localhost;userid=root;pwd=123456;port=3306;database=sensinghub-ncit;sslmode=none;AllowPublicKeyRetrieval=true"
    "Default": "server=192.168.18.7;userid=root;pwd=Monolithiot123!;port=3306;database=storehub;sslmode=none;AllowPublicKeyRetrieval=true"
  },
  "AbpZeroLicenseCode": "00PHkt839UCUnzuJhRPc2mUpaPtu11EoQBc3b8a4fde677e9932e922c0fa4a29565",
  "App": {
    "ServerRootAddress": "http://0.0.0.0:8080/",
    "ClientRootAddress": "http://localhost:4200/",
    "CorsOrigins": "http://192.168.18.7,http://0.0.0.0,http://0.0.0.0:8080,http://192.168.131.135:1883,http://localhost:4200,http://localhost:8080,http://localhost:8081,http://localhost:3000,http://localhost:1881,http://192.168.2.189:21021,http://localhost:21021,http://139.196.240.230,http://localhost:630",
    "AllowAnonymousSignalRConnection": "true"
  },
  "Authentication": {
    "JwtBearer": {
      "IsEnabled": "true",
      "SecurityKey": "SensingHub_C421AAEE0D114E9C",
      "Issuer": "SensingHub",
      "Audience": "SensingHub"
    },
    "DefaultTenant": {
      "TenantId": 2,
      "TenancyName": "panshi",
      "UseMqtt": 0,
      "UseSocket": 0,
      "StoreId": "10874",
      "SensingHubDeviceId": "sensinghub72159",
      "SensingDecisionDeviceId": "sensingdecision72159",
      "GantuDeviceId": "gantu72160",
      "MqttExchange": "amq.topic",
      "Durable": true,
      "VisionFrom": "ncit_tracking",
      "SubKeySettingName": "App.SensingHubSubKey",
      //"SubKey": "34cd01b165564bfeb476244cdac7819b"
      "SubKey": "4364259c9b254aefad179a30bfc97de3"
    }
  },
  "Redis": {
    "ConnectionString": "192.168.3.101:6379,password=1q2w3e4r5t6y,abortConnect=false",
    "InstanceName": "RedisLockInstance"
  },
  "Kestrel": {
    "Endpoints": {
      "Http": {
        "Url": "http://0.0.0.0:8080/"
      }
    }
  },
  "Swagger": {
    "ShowSummaries": false
  },
  "RabbitMQ": {
    "HostName": "192.168.18.9",
    "UserName": "admin",
    "Password": "1q2w3e4r",
    "StoreHubOrderQueue": "sensingHub/decision/tenant-8291/order",
    "ReceiveRobotQueue": "sensing.robot.controller.tenant-5089.event",
    "PublishRobotQueue": "sensing.robot.controller.tenant-5089.message",
    "HubReceiveQueue": ".device.controller.tenant-2.device-sensinghub72159",
    "HubPublishQueue1": ".device.controller.tenant-2.device-sensingdecision72159",
    "HubPublishQueue2": ".device.controller.tenant-2.device-gantu72160"
  },
  "DeviceCenter": {
    "IfUse": 0,
    "ReceiveQueue": "sensing.device.controller.tenant-8277.store-27771",
    "RabbitMQ": {
      "HostName": "139.224.15.28",
      "UserName": "troncell",
      "Password": "1qazTronCell@WSX"
    }
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "Customer": {
    "ifUse": true
  },
  "HealthChecks": {
    "HealthChecksEnabled": true,
    "HealthChecksUI": {
      "HealthChecksUIEnabled": true,
      "HealthChecks": [
        {
          "Uri": "http://localhost:8080/healthCheck"
        }
      ],
      "EvaluationTimeOnSeconds": 10,
      "MinimumSecondsBetweenFailureNotifications": 60
    }
  },
  "TcpClientSettings": {
    "ServerIp": "192.168.0.232",
    "ServerPort": 8888,
    "AutoStart": false
  },
  "StoreUrlSettings": {
    "ProductUrl": "https://product.api.troncell.com",
    "DeviceCenterUrl": "https://devicecenter.api.troncell.com",
    "AdsUrl": "https://ads.api.troncell.com",
    "SmartDeviceUrl": "https://smartdevice.api.troncell.com",
    "ActivityUrl": "https://activity.api.troncell.com",
    "IdentityUrl": "https://identity.api.troncell.com",
    "FaceUrl": "https://face.api.troncell.com",
    "OrderUrl": "https://order.api.troncell.com"
  },
  "AuthUrlSettings": {
    "ifUseThird": true,
    "ThirdPersonNumUrl": "http://192.168.18.8:81/sms/track/storePerson", // 河北
    //    "ThirdPersonNumUrl": "http://192.168.18.9/sms/track/storePerson", // 店内判断人数
    //    "ThirdPersonNumUrl": "http://192.168.1.9:8080/sms/track/storePerson", // ntt
    //    "ThirdPersonNumUrl": "http://192.168.18.7:81/sms/track/storePerson", // 苏州
    "PanshiQrCodeUrl": "http://czmt.d4our.com/api/open/sms/cs/v2/qrcodeAuth",
    "PanshiRfidUrl": "http://czmt.d4our.com/api/open/sms/cs/v2/rfidAuth",
    "NttFaceUrl": "http://192.168.1.9:8080/tyt/cs/faceAuth",
    //    "NttFaceUrl": "http://192.168.1.9:8080/sms/cs/faceAuth",
    "NttQrCodeUrl": "http://192.168.1.9:8080/tyt/cs/v3/qrcodeAuth",
    //    "NttQrCodeUrl": "http://192.168.1.9:8080/sms/cs/v2/qrcodeAuth",
    "ThirdQrCodeUrl": "http://czmt.d4our.com/api/open/sms/cs/v2/qrcodeAuth",
    "ThirdRfidUrl": "http://czmt.d4our.com/api/open/sms/cs/v2/rfidAuth",
    "ThirdFaceUrl": "http://192.168.30.252:48080/app-api/system/user/faceQueryUserInfo"
  }
}
```
### 需要修改的配置及对应配置说明
1. ConnectionStrings下的Default是数据库连接配置，需改成真实的数据库连接地址
2. Authentication下的DefaultTenant的TenantId跟TenancyName需改成云上对应的租户信息
3. UseMqtt改成0就是不连mq，改成1就是要用mq
4. RabbitMQ下的配置就是mq的连接信息
5.  "ReceiveRobotQueue": "sensing.robot.controller.tenant-5089.event",
    "PublishRobotQueue": "sensing.robot.controller.tenant-5089.message",
    "HubReceiveQueue": ".device.controller.tenant-2.device-sensinghub72159",
    "HubPublishQueue1": ".device.controller.tenant-2.device-sensingdecision72159",
    "HubPublishQueue2": ".device.controller.tenant-2.device-gantu72160"
    上面的配置里的tenant-后面的租户信息改成云上对应租户 比如改成tenant-5089
6. 授权接口如果要用客户的 Customer下的ifUse改成true 否则改成false
7. AuthUrlSettings下的授权url, 如果用了客户的接口就改ThirdQrCodeUrl、ThirdRfidUrl、ThirdFaceUrl三个url改为客户自己的url