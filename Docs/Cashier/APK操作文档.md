#  1.Android版

## 1.1 APK安装

安装包地址：\\192.168.3.8\产品发布\Release\Cashier

方案一：adb命令安装

1. 安装adb环境 [参考文档](https://blog.csdn.net/weixin_55018452/article/details/121992202) 
   
2. 连接数据线，机器打开开发者模式

3. 在电脑端打开apk路径，按住shift键，鼠标右击，打开powershell窗口

4. 输入命令：adb install -r .\cash-release.1.0.3.apk（apk名称）

方案二：优盘安装

1. 将apk放入U盘，直接插在机器上
   
2. 识别U盘后，文件管理里打开U盘，双击apk进行安装

## 1.2 打开应用

1.首页：无人操作时显示页面.

  <img style="width:200px" class="right" src="/Docs/Cashier/images/1.jpg" alt="images" />

2.切换设备密钥

操作步骤：

1.长按左下角，弹出设置页面

2.修改Subkey设备密钥

3.点击保存后，重新打APK


  <img style="width:200px" class="right" src="/Docs/Cashier/images/2.jpg" alt="images" />

  3.扫描商品码页面

  
  <img style="width:200px" class="right" src="/Docs/Cashier/images/3.jpg" alt="images" />

  4.扫码后购物车页面

  取消交易：弹框确认是否取消，取消后返回首页

  输入条形码：输入商品条形码后，点击确认，商品在购物车显示

  结算：点击结算，选择支付宝或微信支付
<img style="width:200px" class="right" src="/Docs/Cashier/images/4.jpg" alt="images" />

