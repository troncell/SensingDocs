# 多人体感接物

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO-接接乐.zip

## 1.GameSetting.xml 介绍

开发提供 exe 文件包，在文件夹下 settings 文件夹里有 GameSetting.xml 文件

```
<?xml version="1.0"?>
<Game xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<!-- 游戏说明显示时间-->
  <ExplanationTime>5</ExplanationTime>
  <!-- 游戏时间-->
  <GameTime>60</GameTime>
  <!-- 返回首页时间-->
  <GoBackHome>10</GoBackHome>
  <!--设置游戏时间结束前停止生成物品-->
  <StopCreateThings>5</StopCreateThings>
   <!-- 游戏结束后是否自动退出-->
  <IsGameOverQuit>true</IsGameOverQuit>
     <!-- 接物板离头的距离-->
  <PosOffest>0.9</PosOffest>
     <!-- 每个物品的分数-->
  <FractionalMultiplier>100</FractionalMultiplier>
  <!-- 物品掉落速度，必须负数：往下掉，不能为0和正数-->
  <Gravity>-6</Gravity>
    <!-- 掉落间隔-->
  <DropInterval>0.5</DropInterval>
    <!-- 数值越大，物品粘性越高-->
  <breakList>30</breakList>
  <breakList>20</breakList>
  <breakList>10</breakList>
  <breakList>5</breakList>
  <breakList>1</breakList>
  <!-- 设备证书-->
  <DeviceLicense>Njk0ZjU2NTA1MWZhYmQxNjNmMmM4MmRhNDQwMGU2ZjBhNGE4NTZhOA==</DeviceLicense>
</Game>
```

## 2.设备证书生成

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO-base64.zip

开发提供的文件包下，双击 Fruit.exe，生成证书密钥

## 3.运行游戏

### 3.1 多人接物

1.双击打开文件包里的 KeepCar.exe

![1710137368692](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/ConnectingObjects/1710137368692.png)

2.若配置文件里没有填写证书密钥则会弹框提示，点击 OK，关闭弹框

![1710137430732](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/ConnectingObjects/1710137430732.png)

3.进入游戏说明，倒数结束后进入游戏

![1710137471493](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/ConnectingObjects/1710137471493.png)

4.倒数结束后，开始游戏

多个通道，可以多人一起接物

![1710137577448](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/ConnectingObjects/1710137577448.png)

5.游戏结束后，显示各通道的得分

倒计时结束后，退出游戏

![1710137661498](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/InteractiveGames/image/ConnectingObjects/1710137661498.png)

### 3.2 单人接物

体感接物：通过身体控制购物篮方向，接住掉落的礼物或者商品。得到分数，获取积分或奖品。

![1710137661498](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/UserDocs/%E4%BA%92%E5%8A%A8%E6%B4%BB%E5%8A%A8/images/7.png)
