# 一、 机器上安装apk派样机
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



   （2）串口设备选择：ttyUSB0

    波特率选择：115200 （需要根据不同的设备进行更改）

   <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/2.png" alt="H5images" />

2. 秘钥和链接设置

   步骤：

   （1）输入服务器地址：https://d-gw.api.troncell.com

   （2）输入设备密钥：后台设备subkey

   （3）点击检查设备秘钥后，自动选择互动软件（即设备下活动里的游戏应用），回主页下方的灰色文字可进行核对信息是否正确。文字内容是：对应的设备名称、店铺名称和软件版本号。

   （4）贩卖机选择美斯特蓝牙/光敏/rfid，点击回主页

    <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/3.png" alt="H5images" />



# 三、设置界面
注意：
（1）在首页和补货页面，都可以长按右下角，输入密码跳到其他页面。
（2）在首页，长按右下角或左下角，输入密码后可以进入补货页面进行补货。
（3）默认密码为2021，可进行修改

     修改方法：
     在对应设备下的控制里，在AppPod 设置里输入修改密码
     格式：
    {
      "OpenSettingPassword":"2020"
     }
![输入图片说明](https://images.gitee.com/uploads/images/2021/0909/103540_25c9a0f3_8867015.png "屏幕截图.png")

**文字介绍：**
补货：进入货道补货界面（用不到，无需补货）
上传日志：若贩卖机出现故障，可以点击上传日志
参数设定：返回参数设定界面，可修改服务器地址、设备密钥等信息
退出程序：退出软件
<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Sample/images/Deviceimages/4.png" alt="H5images" />
