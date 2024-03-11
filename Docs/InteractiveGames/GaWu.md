# 体感尬舞

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO-MultiGawu-0.2.zip

人物进入界面，挥手触发游戏。根据飘出的动作指示完成动作，多种动作随机出现

## 1.GameSetting.xml 介绍

```
<?xml version="1.0"?>
<Game xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <!-- 游戏结束时间-->
  <GameTime>60</GameTime>
    <!-- 每一个动作的时间-->
  <ScanTime>10</ScanTime>
  <!-- 介绍文字-->
  <IntrductionText>请各位玩家一起仿屏幕中的人物动作,
  看看我们能通过多少关!</IntrductionText>
  <GameOverText>游戏已结束感谢大家的参与!</GameOverText>
  <IsDebug>True</IsDebug>
   <!-- 游戏结束后是否自动退出-->
  <IsGameOverQuit>1</IsGameOverQuit>
<!-- 设备证书-->
  <DeviceLicense>Njk0ZjU2NTA1MWZhYmQxNjNmMmM4MmRhNDQwMGU2ZjBhNGE4NTZhOA==</DeviceLicense>
  <!-- 元素的位置、大小和透明度-->
  <UIElements>
    <UIElement Id="IndexBody" Left="0" Top="-622" Width="512" Height="512" Alpha="0.6" />
  </UIElements>
</Game>
```

## 2.设备证书生成

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO-base64.zip

开发提供的文件包下，双击 Fruit.exe，生成证书密钥

## 3.运行游戏

1.双击打开文件包里的 MultiGaWu.exe

![1710138558272](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/GaWu/1710138558272.png) 2.若配置文件里没有填写证书密钥则会弹框提示，点击 OK，关闭弹框

![1710137430732](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/ConnectingObjects/1710137430732.png)

3.进入游戏说明，倒数结束后进入游戏
![1710138676004](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/GaWu/1710138676004.png)

4.开始游戏

人物进入界面，挥手触发游戏。根据飘出的动作指示完成动作，多种动作随机出现

![1710138882208](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/GaWu/1710138882208.png)

1. 游戏结束

![1710138852496](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/GaWu/1710138852496.png)
