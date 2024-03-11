# AR 魅影设置

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO/AR 魅影

# 1.AppSetting.xml 介绍

开发提供 exe 文件包，在文件夹下 settings 文件夹里有 AppSetting.xml 文件

```
<?xml version="1.0" encoding="utf-8"?>
<Setting>
  <!--千目api主机头-->
  <ApiHost Value="http://1000my.cn:8896">http://1000my.cn:8896</ApiHost>
  <!--无人进入广告时间-->
  <IdleTime Value="5">5</IdleTime>
  <!--逗留时长算停留-->
  <HaltTime Value="6">6</HaltTime>
  <!--地图文件夹-->
  <MapFolder Value="C:\MapFile">C:\MapFile</MapFolder>
  <!--停车厂文件夹-->
  <ParkFolder Value="C:\ParkFile">C:\ParkFile</ParkFolder>
  <!--最近距离-->
  <MinDistance Value="1">1</MinDistance>
  <!--最远距离-->
  <MaxDistance Value="2">2</MaxDistance>
  <!--游戏缩放-->
  <GameBodyScale Value="2">2</GameBodyScale>
  <!--欢迎词-->
  <WelcomeTexts>
    <WelcomeText>您好</WelcomeText>
    <WelcomeText>Hello</WelcomeText>
    <WelcomeText>欢迎</WelcomeText>
    <WelcomeText>开始互动吧</WelcomeText>
    <WelcomeText>站在中心，放眼未来 </WelcomeText>
  </WelcomeTexts>
</Setting>
```

## 2.运行游戏

虚幻成像场景，有趣的元素：如星光，气泡，蝴蝶等，并可融入品牌元素，支持单人或多人参与，变换手势还会出现不同的动效

![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/UserDocs/%E4%BA%92%E5%8A%A8%E6%B4%BB%E5%8A%A8/images/6.png)
