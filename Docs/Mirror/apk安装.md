# 1. APK安装

方案一：adb命令安装

1. 安装adb环境 [参考文档](https://blog.csdn.net/weixin_55018452/article/details/121992202) 
   
2. 连接数据线，机器打开开发者模式

3. 在电脑端打开apk路径，按住shift键，鼠标右击，打开powershell窗口

4. 输入命令：adb install -r .\com.troncell.sample-v3.0.0-beta06-release.apk（apk名称）

方案二：优盘安装

1. 将apk放入U盘，直接插在机器上
   
2. 识别U盘后，文件管理里打开U盘，双击apk进行安装
   
安装后默认显示两个apk，一个设置参数，一个进入魔镜
# 2登录设备密钥

注意：只有清除数据或者重新安装apk才能看到输入密钥界面

1.双击打开apk

2.输入设备密钥，点击注册

3.等待资源同步完成，进入首页

# 3.打开设置apk
|  参数  |  描述|
|--|--|
|debug|进入debug模式，在魔镜apk的人脸界面可调整相机位置|
|动效|可以添加动效|
|圆形剪切|是否打开圆形剪切，若未打开人脸界面显示方形|
|输入休眠时长|设置休眠时长|
|剪切边距|输入剪切边距|
|输入检测时长|设置检测时长|
|相机偏移X,Y|设置相机偏移位置|


   <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Mirror/images/1.jpg" alt="images" />
   
# 4.调整相机位置
前提：打开debug模式，进入人脸识别界面

可以左移、右移、上移、下移、放大、缩小、重置摄像头

 <img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/Mirror/images/2.jpg" alt="images" />
