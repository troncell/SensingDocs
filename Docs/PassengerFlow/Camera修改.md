乐山客流为例

参考demo NAS地址：\\192.168.3.8\实施交付\2022项目交付备份\项目软件

# 修改Data.xml
1.打开demo文件夹，进入文件夹下Shell\Data，双击Data.xml

![images](/Docs/PassengerFlow/images/8.png)

2.修改ip和添加计数器

```
<!--Camera列表-->
        <Cameras>
        <!-- 摄像头ip和端口 -->
          <Camera Ip="192.168.2.75" Port="2555"/>
        </Cameras>
        <Counters>
        <!-- 添加计数器和对应的计数器名称 -->
          <Counter>Counter 0</Counter>
        </Counters>

```

# 界面显示

访问者信息通过摄像头进行计数

您是第 1 位参访者  

 您是本月第  1 位参访者

 您是今日第  1 位参访者
![images](/Docs/PassengerFlow/images/9.png)