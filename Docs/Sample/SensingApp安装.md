# 自助派样 APK

# 目录

- [自助派样 APK](#自助派样-apk)
- [目录](#目录)
- [一、 机器上安装 apk 派样机](#一-机器上安装-apk-派样机)
- [二、注册密钥](#二注册密钥)
- [三、应用选择](#三应用选择)
- [四、参数设置页面](#四参数设置页面)
- [五、设置界面](#五设置界面)
- [六、补货界面](#六补货界面)

# 一、 机器上安装 apk 派样机

方案一：adb 命令安装

1. 安装 adb 环境 [参考文档](https://blog.csdn.net/weixin_55018452/article/details/121992202)
2. 连接数据线，机器打开开发者模式
3. 在电脑端打开 apk 路径，按住 shift 键，鼠标右击，打开 powershell 窗口
4. 输入命令：adb install -r .\com.troncell.sample-v3.0.0-beta06-release.apk（apk 名称）

方案二：优盘安装

1. 将 apk 放入 U 盘，直接插在机器上
2. 识别 U 盘后，文件管理里打开 U 盘，双击 apk 进行安装

# 二、注册密钥

- 安装完成后，打开 SensingApp
- 输入云平台地址：https://d-gw.api.troncell.com
- 输入 sensinghub 地址：http://192.168.1.7:8080（例）
- 输入设备密钥
- 点击检查设备密钥，可以查看设备信息(租户-店铺-设备名-设备类型-版本号)
- 点击注册，进入应用选择页面

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/image/SensingApp%E5%AE%89%E8%A3%85/1711431618825.png" alt="Deviceimages" />

# 三、应用选择

可以选择对应的应用场景，选择自助派样

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/image/SensingApp%E5%AE%89%E8%A3%85/1711431897024.png" alt="Deviceimages" />

# 四、参数设置页面

1. 调试机器货道：串口设备和波特率设置

   <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/image/SensingApp%E5%AE%89%E8%A3%85/1711432134134.png" alt="Deviceimages" />

   （1）下拉选择互动软件

   （2）串口设备和波特率选择（需要根据不同的贩卖机进行更改）：

| 设备           | vectorFolderName | 波特率 | 串口设备     |
| -------------- | ---------------- | ------ | ------------ |
| 兴元           | xinyuan          | 57600  | dev/ttyS1    |
| 米泉           | miquan           | 9600   | S1           |
| 米泉新版       | miquannew        | 9600   | S1           |
| 伍易           | wuyi             | 19200  | ttyS3        |
| 美斯特         | meisite          | 115200 | ttyUSB0      |
| 因格智能       | yinggezhineng    | 9600   | ttyUSB0      |
| 诺德           | nuode            | 38400  | ttyUSB0      |
| 九方汇（RFID） | jiufanghui       | 57600  | dev/ttyUSER6 |

    （3）打开串口设置进行串口调试

    点击命令列表的货道，查看是否掉货成功，成功后回到参数设定页面

<img style="width:400px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/2.png" alt="H5images" />

(4)点击回首页，显示大屏首页

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/6.png" alt="H5images" />

# 五、设置界面

注意：
（1）在首页和补货页面，都可以长按右下角，输入密码跳到其他页面。
（2）在首页，长按右下角或左下角，输入密码后可以进入补货页面进行补货。
（3）默认密码为 2021，可进行修改

    修改方法：
     在对应设备下的控制里，在AppPod 设置里输入修改密码
     格式：
    {
      "OpenSettingPassword":"2020"
     }![输入图片说明](https://images.gitee.com/uploads/images/2021/0909/103540_25c9a0f3_8867015.png "屏幕截图.png")

**弹框选项：**

设备注册：可修改服务器地址、设备密钥等信息

补货：进入货道补货界面

上传日志：若贩卖机出现故障，可以点击上传日志

应用选择：进入应用选择页面

参数设置：返回参数设置界面

退出程序：退出软件

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/image/SensingApp%E5%AE%89%E8%A3%85/1711433351647.png" alt="Deviceimages" />

# 六、补货界面

![](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/5.png)

webview 内核版本查看
在设置界面的主界面地址里输入：https://liulanmi.com/labs/core.html 后点击回首页，显示 webview 版本，当 webview 版本过低时需要进行升级
