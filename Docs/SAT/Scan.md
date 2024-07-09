# 软件介绍

## 1.启动软件弹框

### 1.1 启动扫描软件，硬件异常弹框

打开软件，相关硬件设备异常会弹框显示。单击确定软件退出，确保硬件打开后再打开软件
![1720495077498](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720495077498.png)

### 1.2 初始化（机械轴回原点）

![1720494882907](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720494882907.png)

1. 单击 YES，开始初始化，等待初始化完成

![Scan3](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片3.png)![Scan4](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片4.png)

（2）单击 NO，弹框消失，默认当前位置为原点

（3）单击 Cancel，退出应用

## 2.菜单栏：文件

### 2.1 读取扫描

操作步骤：单击文件-点击读取-选择 isd 文件-点击确定

可以读取之前保存的扫描（isd）文件，包含：成像、扫描设置等信息

![Scan6](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片6.png)

### 2.2 另存为扫描

另存为本次的扫描设定和结果(.isd)文件

操作步骤：扫描结束后-单击文件-点击另存为-输入文件名名-点击确定

## 3.菜单栏：设置

### 3.1 数据转换设置

**采集卡的设定：**

可设置取样率：1000 取样率越高，采样数据越多

可设置频道 A/B 的信号设定 耦合：AC 模拟信号 DC：数字信号

输入范围：选择输入电压范围 例如设定 400 毫伏，总振幅电压范围为 400\*2=800 毫伏

![1720505759380](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720505759380.png)

### 3.2 发射器设定

**超声波发射器信息设定：**

1. 打开 ch.A 或 ch.B
2. 模式：回声/穿透模式切换
3. 触发器：选择内部触发或外部触发，默认选择外部触发
4. PRF 频率：内部触发时，发射超声的频率设定
5. 电压：330V 电压越高，超声波发射能量越大
6. 减幅：50 调节信号大小（振幅变小，频率变高的现象），
7. 能量：low 设定电压总能量，能量越高，波形振幅更大
8. 增益：可调节整体波形振幅的大小
9. 调整低通滤波：50MHz 例如设置 50Mhz，表示低于 50Mhz 以内的波形让它通过，高于 50Mhz 以上的波形过滤掉 （看实际的产品和反射波行）

（10）高通滤波：2.5MHz 例如设置 2.5Mhz，表示高于 2.5Mhz 的波形让它通过，低于 2.5Mhz 的波形过滤掉

![1720507314906](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720507314906.png)

### 3.3 设定

Mm 刻度按钮：设定波形图是以时间还是刻度为单位，可进行切换

设置水传播速度和材料传播速度

![1720507367116](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720507367116.png)

### 3.4 设置

#### 3.4.1 基础设置

设置是否启动自动传输:扫描结束后，自动保存文件并将数据传送至自动解析软件解析软件

分析软件地址：自动解析软件路径地址

自动保存路径：条件：自动保存按钮打开。扫描结束后，文件自动保存地址。

自动保存扫描：是否打开自动保存按钮，若打开，自动保存地址已填，扫描结束后会将文件自动保存至设置的路径。若不打开，扫描结束后不会自动保存文件

人工分析跳转：打开按钮，扫描结束后，自动保存文件并将数据传送人工解析界面进行判定。关闭按钮，则不会跳转至人工解析界面，可手动点击人工解析按钮进入。

![1720507505287](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720507505287.png)

传输弹框：

![Scan19](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片19.png)
**人工判定弹框（手动）：**

点击是：数据自动传输至人工判定界面

点击否：弹出自动保存的路径后，关闭弹框

**人工判定弹框（自动）：**

点击是：数据自动传输至人工判定界面，关闭弹框，并且将分割后的图片保存到配置的文件夹下

点击否：关闭弹框，数据不会传输至人工判定界面。

#### 3.4.2 IO 设置

是否启用水泵：控制点击开始扫描后是否打开水泵

## 4.菜单栏：人工分析

功能说明：判定的功能是为了扫描样品结束后，能够快速的对样品的好坏进行判定。目前判定支持人工判定和第三方 AI 判定。

### 4.1 扫描界面：

1.序列号录入：动态格式可在配置文件 System.ini 里进行配置：

Special, SerialFormatTemplate, {$Model}\_{$Serial}

Model:电池型号 Serial：序列号

1.正面和反面选择：扫描前选择 Top 或 Btm ，文件传输后可知晓扫描的是正面或反面

![Scan9](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片9.png)

### 4.2 判定界面：

1.支持通道和数据类型选择:判定界面支持单探头和双探头通道，可切换对应的闸门和数据类型

2.显示对应序列号：扫描界面的备注框里按顺序输入样品序列号，传输至判定界面后序列号与扫描样品对应

3.支持读取文件：若自动传输文件选择取消，后面可通过读取文件重新判定

4.支持 UNC、OK、NG 三种判定

5.统计当前判定总数，统计各判定结果的数量

6.检测模式：手动和自动

7.配置路径支持动态参数，详细参数请参照下文的参数列表

配置的文件路径为:

C:\Users\Administrator\AppData\Roming\NDTSCAN

**（ 1 ）手动：人工判定**

在判定界面进行人工判定，判定后点击保存结果

判定后可保存判定后的图片和 csv 文件，存储路径可在配置文件 system.ini 进行配置：

**Csv 动态路径：**

**PersonAnalysis,PersonAnalysisResultCsvSavePath,**

D:\\CSV\\{$ShortYear}{$Month}{$Day}\\{$MachineNumber}\\{$HHMMSS}\_{$MachineNumber}\_\_AI_judge_result.csv

![Scan10](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片10.png)

![Scan11](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片11.png)

**Image 动态路径 :**

**PersonAnalysis, PersonAnalysisResultImageSavePath,**

D:\\Img\\{$ShortYear}{$Month}{$Day}\\{$MachineNumber}\\{$Surface}\\{$Result}\\{$HHMMSS}\_{$MachineNumber}\_{$Layer}\_{$Surface}\_{$Model}\_{$Serial}.bmp

![Scan12](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片12.png)

### 4.3 动态参数列表：

**动态路径变量：**

变量的格式必须是{$VariableName}

具体的变量如下:

Year：年 如：2022

ShortYear：短年 如：22

Month：月 如：11

Day：日 如：dd

MachineNumber：机器编号：01

HHMMSS：时分秒

Layer：(1-channel)(1-gate)(2-slice)(1-type)：通道闸门切片类型

如：12031 1=ChA 2=DATA2 03=切片 3 0=数据类型为 AbsPeak 1=数据类型为 AbsTof 2=数据类型为 FallingEdge 3=数据类型为 RasingEdge

Surface：Top 或 Btm 等

Model: 样品型号

Serial：序列号

Bmp：图片格式 例如：bpm、jpg、png

Result：结果 如：OK、NG、UNC

Confidence：结果可信度 如：80

## 5.扫描设置

![1720508277389](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720508277389.png)

### 5.1 手动控制 ：控制 X 、 Y 、 Z 轴的移动

1. 选择您想移动轴的速度
2. 左右移动 X 轴，在 X 轴上，让探头移至样品的中心
3. 上下移动 Y 轴，在 Y 轴上，让探头移至样品的中心

**说明** ：index 模式： 中间框输入值，单击箭头，轴向对应方向移动对应的值

    jog 模式：中间为空，长按箭头，轴以对应速度向对应方向移动

### 5.2 初始化：初始化所有的轴到默认位置

点击初始化，机械轴初始化运动回到原点，等待初始化完成

![Scan8](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/images/Scanimages/图片8.png)

### 5.3 扫描和分辨率

#### 5.3.1 线性扫描

扫描类型：可选择扫描类型为线性扫描

单向：可设置扫描时是单向扫描还是双向扫描

产品大小：可设置扫描产品的大小

扫描分辨率：可设置扫描分辨率，分辨率越小, 像素越高

#### 5.3.2 托盘扫描

![1720508468959](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720508468959.png)

扫描类型：可选择扫描类型为托盘扫描

单向：可设置扫描时是单向扫描还是双向扫描

产品大小：可设置扫描产品的大小

跳跃：可设置 X、Y 方向的产品之间的间隔

数量：可设置 X、Y 方向的产品数量

扫描模式：可设置单个扫描模式(暂时只能行扫)

扫描分辨率：可设置扫描分辨率，分辨率越小, 像素越高

### 5.4 设置中心位置

将探头移至样品上，表面跟踪线闸在样品表面波上，设置探测位置，点击探测样品大小，会自动识别到样品大小和中心位置

### 5.5 快捷操作

设扫描结束位置：设定扫描结束后，探头移动到的停留位置

移扫描结束位置：设定结束位置后，点击移扫描结束位置，探头会快速移至设扫描结束位置

设定中心：样品已经移动至探头的中心后，点击设定中心按钮。

移至中心：设定中心后，若后面探头不在中心位置，可点击移至中心，探头会快速移至中心位置

设定焦距：找到最佳焦距后，点击设定焦距

移至焦距：设定焦距后，如 z 轴移动到其他位置，可点击移至焦距，探头会快速移至焦距位置

## 6.扫描控制

![1720509301507](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720509301507.png)

### 6.1 开始扫描

**参数设定后可以开始扫描：**

1.扫描参数设定：

（1）设定中心（X\Y 轴）：探头移动至样品中心

（2）设定焦距（Z 轴）：探头移动至最佳焦距

（3）设定样品大小

（4）设定分辨率

（5）设定表面跟踪线 FSF 和闸门 DATA

2.参数设定后，可以点击开始扫描按钮，开始扫描

### 6.2 暂停扫描

扫瞄时, 点击暂停扫描按钮, 则暂停;再点击继续扫描, 则继续。

### 6.3 停止扫描

扫瞄时,点击停止扫描 , 则中止扫瞄

### 6.4 扫描速度

速度：设置扫描时的速度

加速度：设置扫描时的加速度

## 7.闸门

![1720509671156](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720509671156.png)

### 7.1 频道

切换 Channel 显示波形：可以打开频道 A 或频道 B，或者两者都打开

### 7.2 闸门

**勾选闸门，波形图下方显示闸门，不勾选，波形图下方不显示闸门**

| 字段     | 描述                                                                                                                                                         |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| FSF      | 表面跟踪先，样品置于不平的情况下，探头接收表面返回的超声波所需的时间不同，FSF 表面跟踪功能可以在接收到表面返回声波后通过固定的时间间隔来获取同意层面的图片， |
| DATA     | 采集产品表面或者里面的数据，可以有多个 DATA                                                                                                                  |
| 开关     | 是否启用 FSF 和 DATA                                                                                                                                         |
| 跟随     | DATA 选择跟随 FSF，跟随后 DATA 跟随 FSF 显示                                                                                                                 |
| 延缓     | 调整 FSF 或 DATA，延缓跟随变换                                                                                                                               |
| 高度     | 调整 FSF 或 DATA，高度跟随变换                                                                                                                               |
| 长度     | 调整 FSF 或 DATA，长度跟随变换                                                                                                                               |
| 切片数   | DATA 分成对应的份数                                                                                                                                          |
| 数据类型 | 计算勾选的数据类型，可以勾选 TOF、peak、falling、rising                                                                                                      |

## 8.波形区

![1720510119335](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720510119335.png)

### 8.1 表面跟踪

勾选表面跟踪，在移动探头（上下）时（波形左右会移动）

Data 等区域会以 Fsf 为基准，跟随波形移动.一般用于调整焦距

### 8.2 波形叠加

勾选波形叠加：Ascan 的波形扫描前重复叠加

### 8.3 峰值显示

峰值隐藏：所有 DATA 的峰值不显示

峰值显示：所有 DATA 的峰值显示

峰值选中：显示选中 DATA 的峰值

| 字段     | 描述                                       |
| -------- | ------------------------------------------ |
| 中心位置 | 将 FSF 和 DATA 展现在波形中间              |
| 数字增益 | 改变软件里波形的增益值，相当于放大缩小波形 |
| 模拟增益 | 改变硬里件波形的增益值，相当于放大缩小波形 |
| 保存图片 | 保存波形图                                 |
| 保存数据 | 保存波形数据                               |

## 9.显示区

![1720510374768](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720510374768.png)

### 8.1 左侧功能注释

| 数据通道      | 切换数据通道                                                           |
| ------------- | ---------------------------------------------------------------------- |
| GaTa 数据类型 | 切换 TOF、peak、falling、rising，会切换不同成像                        |
| 放大率显示    | 修改成像分辨率                                                         |
| 还原大小      | 成像变成原始大小                                                       |
| 扫描区间      | 扫完之后，针对某一小的区域进行扫描，图像上匡出长方形区域，可以重新扫描 |
| 探头移动      | 在图像上按下某个键，探头会直接移动到这个点位上                         |
| 测量          | 成像区测量长和宽的长度                                                 |
| 图形保存      | 保存成像图，可以保存当前成像图或保存所有成像图                         |
| 图像数据保存  | 保存成像数据为 tiff 格式                                               |
| 备注          | 填写序列号或其他信息                                                   |
| 颜色百分比    | 调整成像颜色                                                           |
| 序列号        | 填写扫描样品型号                                                       |
| 模式切换      | 图片切换模式，不以像素显示                                             |
| Bscan         | 直线波动图，区域波动图、波形统和图                                     |

### 8.2 颜色条

![1720511984195](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720511984195.png)

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

## 7.扫描状态和当前位置

![1720512010182](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SAT/image/Scan/1720512010182.png)

### 7.1 扫描状态

当前状态：扫描未开始、扫描中、扫描结束

扫描进度：实时显示扫描进度

### 7.2 扫描控制

开始扫描：参数设定后，可以点击开始扫描按钮，开始扫描

暂停扫描：扫瞄时, 点击暂停扫描按钮, 则暂停;再点击继续扫描, 则继续。扫瞄时, 点击暂停扫描按钮, 则暂停;再点击继续扫描, 则继续。

停止扫描：扫瞄时,点击停止扫描 , 则中止扫瞄

### 7.3 当前位置

当前位置：实时显示当前探头所在位置
