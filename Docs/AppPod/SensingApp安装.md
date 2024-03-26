## 1.Android 版

### 1.1 APK 安装

方案一：adb 命令安装

1. 安装 adb 环境 [参考文档](https://blog.csdn.net/weixin_55018452/article/details/121992202)
2. 连接数据线，机器打开开发者模式
3. 在电脑端打开 apk 路径，按住 shift 键，鼠标右击，打开 powershell 窗口
4. 输入命令：adb install -r .\com.troncell.sample-v3.0.0-beta06-release.apk（apk 名称）

方案二：优盘安装

1. 将 apk 放入 U 盘，直接插在机器上
2. 识别 U 盘后，文件管理里打开 U 盘，双击 apk 进行安装

### 1.2 登录设备密钥

1. 安装完成后，打开 SensingApp
2. 输入云平台地址：https://d-gw.api.troncell.com
3. 输入 sensinghub 地址：http://192.168.1.7:8080（例）
4. 输入设备密钥
5. 点击检查设备密钥，可以查看设备信息(租户-店铺-设备名-设备类型-版本号))
6. 点击注册，进入应用选择页面

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/AppPod/image/SensingApp%E5%AE%89%E8%A3%85/1711420793904.png" alt="Deviceimages" />

### 1.3 应用选择

可以选择对应的应用场景，选择信息发布

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/AppPod/image/SensingApp%E5%AE%89%E8%A3%85/1711423260388.png" alt="Deviceimages" />

### 1.4 信息拉取

选择应用场景后，会提示正在同步资源（注：若修改了信息，并将信息重新发布到了设备，需要在 sensingstore 的后台，设备下的控制里，点击更新资源，机器会提示正在同步资源）

### 1.5 设置弹框

**1.密码设置**

在首页和补货页面，都可以长按右下角，输入密码跳到其他页面。

默认密码为 2021，可进行修改

修改方法：
在对应设备下的控制里，在 AppPod 设置里输入修改密码
格式：
{
"OpenSettingPassword":"2020"
}

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/AppPod/image/SensingApp%E5%AE%89%E8%A3%85/1711424325232.png" alt="Deviceimages" />

**2.弹框选项**

设备注册：可修改服务器地址、设备密钥等信息

上传日志：若贩卖机出现故障，可以点击上传日志

应用选择：进入应用选择页面

参数设置：返回参数设置界面

退出程序：退出软件

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/AppPod/image/SensingApp%E5%AE%89%E8%A3%85/1711424512731.png" alt="Deviceimages" />

### 1.6 调试页面

（1）广告信息：打开广告信息，再进入播放界面，下方会显示具体播放信息

（2）Debug：打开 Debug，再进入播放界面，播放 H5 内容时下拉可以刷新页面。关闭 Debug，播放 H5 页面下拉不会刷新。

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/AppPod/image/SensingApp%E5%AE%89%E8%A3%85/1711424185606.png" alt="Deviceimages" />
