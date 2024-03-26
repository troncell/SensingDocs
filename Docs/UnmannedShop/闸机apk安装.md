- [1. 安装和测试闸门](#1-安装和测试闸门)
  - [1.1 安装闸门](#11-安装闸门)
  - [1.2 登录设备密钥](#12-登录设备密钥)
  - [1.3 应用选择](#13-应用选择)
  - [1.4 进入闸机首页](#14-进入闸机首页)
  - [1.5 设置弹框](#15-设置弹框)
  - [1.6 参数设置页面](#16-参数设置页面)
- [2.闸门测试](#2闸门测试)
- [3. 异常情况](#3-异常情况)

# 1. 安装和测试闸门

## 1.1 安装闸门

1. 安装 sensingapp.apk ，可以放在 U 盘里插入机器上安装，或者通过命令安装：adb install -r .\sensingapp.apk

## 1.2 登录设备密钥

1. 安装完成后，打开 SensingApp
2. 输入云平台地址：https://d-gw.api.troncell.com
3. 输入 sensinghub 地址：http://192.168.1.7:8080（例）
4. 输入设备密钥
5. 点击检查设备密钥，可以查看设备信息(租户-店铺-设备名-设备类型-版本号))
6. 点击注册，进入应用选择页面
7. 进入闸门软件后，点击左下角进入配置界面

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/UnmannedShop/image/%E9%97%B8%E6%9C%BAapk%E5%AE%89%E8%A3%85/1711438944635.png" alt="Deviceimages" />

## 1.3 应用选择

可以选择对应的应用场景，选择智能闸机

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/UnmannedShop/image/%E9%97%B8%E6%9C%BAapk%E5%AE%89%E8%A3%85/1711439406506.png" alt="Deviceimages" />

## 1.4 进入闸机首页

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/UnmannedShop/image/%E9%97%B8%E6%9C%BAapk%E5%AE%89%E8%A3%85/1711439716386.png" alt="Deviceimages" />

如果 hub 未填写或者未成功连接，页面右下角会显示红色字体：hub 未连接

开机若需要自启动，需要在机器里设置

## 1.5 设置弹框

在首页和补货页面，都可以长按右下角，输入密码跳到其他页面。

默认密码为 2021，可进行修改

修改方法：
在对应设备下的控制里，在 AppPod 设置里输入修改密码
格式：
{
"OpenSettingPassword":"2020"
}

**弹框选项：**

设备注册：可修改服务器地址、设备密钥等信息

补货：进入货道补货界面

上传日志：若贩卖机出现故障，可以点击上传日志

应用选择：进入应用选择页面

参数设置：返回参数设置界面

退出程序：退出软件

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/UnmannedShop/image/%E9%97%B8%E6%9C%BAapk%E5%AE%89%E8%A3%85/1711439936297.png" alt="Deviceimages" />

## 1.6 参数设置页面

<img style="width:200px" class="right" src="https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/UnmannedShop/image/%E9%97%B8%E6%9C%BAapk%E5%AE%89%E8%A3%85/1711440110678.png" alt="Deviceimages" />

无人操作时间：设置无人操作时间，无人识别，几秒后回到首页

百度人脸密钥：百度人脸密钥

游戏密钥：后台设备下的游戏密钥

人脸识别：人脸识别 url，可以勾选是否启用人脸识别，url 由开发提供

二维码识别：：二维码识别 url，可以勾选是否启用二维码识别，url 由开发提供

IC 卡识别:IC 卡识别 url，可以勾选是否启用 IC 卡识别，url 由开发提供

# 2.闸门测试

1. 扫描正确的二维码

   提示：人脸/扫码核验通过

2. 扫描失效的二维码

   提示：验证失败，请重试

3. 店铺人数已满

   提示：当前店铺人数已满，请稍后再进

4. 非营业时间扫码

   提示：当前时间为非营业时间

5. 店铺维护中

   提示：店铺正在维护，暂停营业

6. 用户存在未支付的订单

   提示：您有未支付的订单

# 3. 异常情况

情况 1：若出现连接事件线后门自动打开，可能是后台进程开的太多

解决方案：需要关掉后台所有进程，再重新打开软件
