# 切水果体感游戏

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO-切水果.zip

## 1.GameSetting.xml 介绍

开发提供 exe 文件包，在文件夹下 settings 文件夹里有 GameSetting.xml 文件

```
<?xml version="1.0"?>
<Game xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
 <!-- 游戏说明显示时间-->
  <GameIntroCountdownTime>10</GameIntroCountdownTime>
   <!-- 游戏开始倒数时间-->
  <GameStartCountdownTime>3</GameStartCountdownTime>
   <!-- 游戏结束时间-->
  <GameEndCountdownTime>10</GameEndCountdownTime>
   <!-- 游戏结束时间后面的文字-->
  <GameEndCountdownText>S后返回首页</GameEndCountdownText>
  <!-- 游戏时间-->
  <GameTime>60</GameTime>
   <!-- 切到水果的得分-->
  <CutFruitScore>1</CutFruitScore>
   <!-- 每次最多生成的水果数量-->
  <MaxSpawnFruitCountsPerTimes>5</MaxSpawnFruitCountsPerTimes>
   <!-- 切到炸弹扣除的分数-->
  <CutBoomScore>5</CutBoomScore>
  <!-- 水果水平的力（一般无需改动）-->
  <FruitForceX>1000</FruitForceX>
    <!-- 水果向上的力（一般无需改动）-->
  <FruitForceY>7000</FruitForceY>
   <!-- 游戏结束后是否自动退出-->
  <IsGameOverQuit>false</IsGameOverQuit>
  <IsDebug>false</IsDebug>
   <!-- 设备证书-->
  <DeviceLicense>Njk0ZjU2NTA1MWZhYmQxNjNmMmM4MmRhNDQwMGU2ZjBhNGE4NTZhOA==</DeviceLicense>
</Game>
```

## 2.设备证书生成

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO-base64.zip

开发提供的文件包下，双击 Fruit.exe，生成证书密钥

![1710125822122](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/Fruit/1710125822122.png)

## 3.运行游戏

1.双击打开文件包里的 Fruit.exe

![1710128768062](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/Fruit/1710128768062.png)

2.若配置文件里没有填写证书密钥则会弹框提示，点击 OK，关闭弹框

![1710128915878](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/Fruit/1710128915878.png)

3.进入游戏说明，倒数结束后进入游戏

![1710128993943](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/Fruit/1710128993943.png)

4.倒数结束后，开始游戏

多个通道，可以多人一起切水果，切到水果加分，切到炸弹减分

![1710129122584](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/Fruit/1710129122584.png)

5.游戏结束后，显示各通道的得分

倒计时结束后，回到首页继续轮循

![1710129266346](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/Fruit/1710129266346.png)
