# 软件介绍

## 1.启动分析软件

### 1.1 启动分析软件

打开软件，进入分析软件。

![1720512243931](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720512243931.png)

## 2.文件

读取：单击右上角文件图标，点击读取，选择需要分析的 isd 文件，点击确定

保存：单击右上角文件图标，点击保存，保存修改后的数据

另存为：单击右上角文件图标，点击另存为，保存新的文件

![1720512976327](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720512976327.png)

## 3.扫描图片

扫描图片：显示扫描时保存的不同通道和类型的图片，单击一个图片，右侧显示显示图片

![1720512986098](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720512986098.png)

## 4.参数信息

1.Recipe: 扫描样品时的设置信息

![1720513516463](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720513516463.png)

2.P/R-Ch.A 和 P/R-Ch.B ： dpr 设置信息

![1720513539179](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720513539179.png)

## 5.标注列表

显示图片上框选的区域列表

![1720513693448](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720513693448.png)

## 6.设置阈值和判断条件

### **6.1 缺陷参数设置：**

振幅区间：设置振幅区间

缺陷间隔：设置缺陷间的间隔，最小间隔 0.1

最小缺陷面积：设置最小缺陷面积，最小缺陷面积 0.01

是否包含无数据：是否包含无数据内容

执行按钮：点击开始，执行参数

### 6.2 判定条件

勾选的条件参与判定 ，若未勾选则不参与判定

总缺陷面积占比：判断每个 ROI 总缺陷面积占比大于阈值则为 OK 或 NG

缺陷个数：判断每个 ROI 总缺陷个数大于阈值则为 OK 或 NG

缺陷总面积：判断每个 ROI 总缺陷面积大于阈值则为 OK 或 NG

最大单个缺陷面积：判断每个 ROI 最大缺陷面积大于阈值则为 OK 或 NG

逻辑：ROI 所有判定为 OK，则 ROI 的结果为 OK；若 ROI 所有判定条件有一个为 NG，则 ROI 的结果为 NG

执行判定按钮：设置完判定条件，点击开始判定

![1720513887340](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720513887340.png)

## 7. 显示区

![1720515055640](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515055640.png)

### 7.1 左侧图标：ROI

![1720514502205](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514502205.png) 箭头：选中 roi 框

![1720514536951](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514536951.png) 方形：框选区域为正方形

![1720514551901](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514551901.png) 圆形：框选区域为圆形

![1720514564318](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514564318.png) 钢笔：自定义框选区域

![1720514575630](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514575630.png) 魔术棒：自动框选一个区域

![1720514598331](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514598331.png) 自动框选：自动框选样品上的区域

![1720514617560](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514617560.png) 添加：框选区域后，需要点击添加按钮，否则为未框选

![1720514626636](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514626636.png) 删除：选中框选区域后，点击删除按钮，可删除选中的区域

![1720514638476](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514638476.png) 全部删除：箭头选中状态下，点击全部删除，可删除所有框选区域（删除所有 ROI）

![1720514669822](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514669822.png) 底色：点击底色按钮，所有框选的 roi 底色会不显示

### 7.2 右侧图标

![1720514755991](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514755991.png)选中箭头：可以选中 roi 框删除框选区域

![1720514767283](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514767283.png)自适应：成像变成原始大小

![1720514775066](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514775066.png)测量：成像区测量长度

![1720514784907](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514784907.png)二位测量：测量长和宽的长度

![1720514796100](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514796100.png)Bscan：显示 Bscan 成像

![1720514806305](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720514806305.png)保存：保存图片

### 7.3 颜色条

| 轮廓线       | 设置轮廓线的颜色                                     |
| ------------ | ---------------------------------------------------- |
| 无数据       | 设置无数据显示的颜色                                 |
| 同步         | 有多个切片数时，勾选同步，可以一键修改所有切片的颜色 |
| 添加颜色     | 当前显示的颜色条添加其他颜色                         |
| 添加阈值颜色 | 当前显示的颜色条添加阈值颜色                         |
| 层次         | 颜色条渐变线性或渐变实心显示                         |
| 对称模式     | 设置对称性或非对称性显示                             |
| 系统选项版   | 设置默认、彩虹、层次、相位反转显示                   |
| 用户选项版   | 可添加调色板和保存调色板                             |
| 显示刻度     | 设置是否显示刻度                                     |

## 8.缺陷概览

缺陷概览：执行后显示所有 ROI 的缺陷数量、面积以及占比

图片：每个 ROI 上方显示各自缺陷占比以及缺陷数量

![1720515240050](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515240050.png)

## 9.缺陷详情

显示所有框选区域的缺陷详情

![1720515332907](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515332907.png)

## 10.判定结果

![1720515623460](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515623460.png)

### 10.1 判定统计

![1720515734658](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515734658.png) 显示总 ROI 数量

![1720515746766](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515746766.png) 显示 ROI 判定为 OK 的数量

![1720515759342](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515759342.png) 显示 ROI 判定为 NG 的数量

### 10.2 roi 详情

显示选中 ROI 判定详情

![1720515786127](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720515786127.png)

## 11.判定详情

显示每个 ROI 判定条件以及对应的结果

![1720516123697](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720516123697.png)

## 12.生成报告

1.选择生成报告内容：分析结果和分析整体概况

2.输入报告信息：样品名称、样品编号、检测机器、检测日期、检测单位、报告页面

3.点击生成报告

4.导出 pdf 文件

![1720516259215](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Analysis/1720516259215.png)
