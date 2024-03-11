# 体感答题

文件包 NAS 地址：/实施交付/2023 项目交付备份/创思 DEMO/体感游戏 DEMO/体感答题

# 1.GameSetting.xml 介绍

开发提供 exe 文件包，在文件夹下 settings 文件夹里有 GameSetting.xml 介绍

```

<?xml version="1.0"?>

-<Game xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<!-- 答题数量 -->
<QuestionCount>5</QuestionCount>

<!-- 下一题时间 -->
<NextQuestionTime>3</NextQuestionTime>

<!-- 回答问题时间 -->
<AnswerTime>30</AnswerTime>

<!-- 结束等待时间 -->
<GameOverWaitTime>5</GameOverWaitTime>

<!-- 设备密钥 -->
<Subkey>3533e597f0734d0081103e8de238155d</Subkey>

<!-- 试卷标签 -->
<PaperTag>2021试卷</PaperTag>

<BodyView Color="#88f7aa63" OffsetY="0" OffsetX="800" Scale="0.5"/>

</Game>

```

## 2.运行游戏

体感答题：通过双手抱拳和双手举过头顶来判断题目的对错

![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/UserDocs/%E4%BA%92%E5%8A%A8%E6%B4%BB%E5%8A%A8/images/8.png)
