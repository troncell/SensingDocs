#  1.Android版

## 1.1 APK安装

apk地址：\\192.168.3.8\产品发布\Release\Cashier

方案一：adb命令安装

1. 安装adb环境 [参考文档](https://blog.csdn.net/weixin_55018452/article/details/121992202) 
   
2. 连接数据线，机器打开开发者模式

3. 在电脑端打开apk路径，按住shift键，鼠标右击，打开powershell窗口

4. 输入命令：adb install -r .\cash-release.1.0.3.apk（apk名称）

方案二：优盘安装

1. 将apk放入U盘，直接插在机器上
   
2. 识别U盘后，文件管理里打开U盘，双击apk进行安装

## 1.2 打开应用

1.首页：无人操作时屏保页面.

  <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Cashier/images/1.jpg" alt="images" />

2.切换设备密钥

操作步骤：

1.长按左下角或者从左向右滑动，弹出设置页面

2.修改Subkey设备密钥

3.点击保存后，重新打开APK


  <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Cashier/images/2.jpg" alt="images" />



# 2.H5版

## 2.1 apk安装
# 一、 机器上安装apk派样机
采用派样机Sample外壳

方案一：adb命令安装  

1. 安装adb环境 [参考文档](https://blog.csdn.net/weixin_55018452/article/details/121992202) 
   
2. 连接数据线，机器打开开发者模式

3. 在电脑端打开apk路径，按住shift键，鼠标右击，打开powershell窗口

4. 输入命令：adb install -r .\com.troncell.sample-v3.0.0-beta06-release.apk（apk名称）

方案二：优盘安装

1. 将apk放入U盘，直接插在机器上
   
2. 识别U盘后，文件管理里打开U盘，双击apk进行安装

# 二、打开apk进行设置

1. 调试机器货道：串口设备和波特率设置

   （1）单击页面右下角图标

   <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/1.png" alt="H5images" />



   （2）串口设备和波特率选择（需要根据不同的贩卖机进行更改）：

| 设备   | vectorFolderName | 波特率    |串口设备|
|------|------------------|--------|-------|
|九方汇（RFID）|jiufanghui|57600|dev/ttyUSER6|

   <img style="width:400px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Cashier/images/6.jpg" alt="H5images" />

2. 秘钥和链接设置

   步骤：

   （1）输入服务器地址：https://d-gw.api.troncell.com

   （2）输入设备密钥：后台设备subkey

   （3）点击检查设备秘钥后，自动选择互动软件（即设备下活动里的游戏应用），回主页下方的灰色文字可进行核对信息是否正确。文字内容是：对应的设备名称、店铺名称和软件版本号。

   （4）选择对应贩卖机,目前自助收银接的是九方汇，选择九方汇，点击回主页

    <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Cashier/images/7.jpg" alt="H5images" />

   (5)显示收银屏保页