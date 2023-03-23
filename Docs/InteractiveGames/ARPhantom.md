# AR魅影设置
#  AppSetting.xml介绍
开发提供exe文件包，在文件夹下settings文件夹里有AppSetting.xml文件

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