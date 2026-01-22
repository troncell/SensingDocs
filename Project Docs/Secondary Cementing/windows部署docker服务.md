### 默认docker desktop装好了

### 先部署数据库 pgsql
``` 
创建持久化卷
执行下面两条命令
docker volume create pgdata
docker run -d --name postgres -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=123456 -e POSTGRES_DB=ergu -p 5432:5432 -v pgdata:/var/lib/postgresql/data postgres:16

```
### 部署后台服务
```
拉取公司云镜像
登录阿里云
docker login --username=qule@1120777826858507 registry.cn-shanghai.aliyuncs.com
密码1qaz@WSX
拉取镜像

docker pull registry.cn-shanghai.aliyuncs.com/troncellapi/sensinghub:v3
注：下面D:/troncell/publish/换成自己的路径
docker run -d --restart always --ulimit core=0 -p 8080:8080 -v D:/troncell/publish/sensinghub/publish:/app -e TZ=Asia/Shanghai registry.cn-shanghai.aliyuncs.com/troncellapi/sensinghub:v3

```

### 部署前台服务
创建一个前端配置文件default.conf并复制保存
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
        proxy_pass http://172.17.0.1:8080/api;
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

    location /AbpUserConfiguration/GetAll {
        # Proxy settings
        proxy_pass http://172.17.0.1:8080/AbpUserConfiguration/GetAll;
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

解压前端dist文件，记住dist文件跟default.conf的路径 更改下面的命令中的路径为自己的
其中D:/troncell/conf就是default.conf所在目录
docker run -d --restart always -v D:/troncell/conf:/etc/nginx/conf.d -v D:/troncell/dist:/usr/share/nginx/html -p 80:80 nginx:1.21
