# 后台介绍

sensingstore 是一个用于管理和运营商户的服务平台，它不仅可以帮助商户接入各种支付、营销、账户、产品等服务，还可以查看和分析平台的数据，管理平台的设备、店铺、会员、广告、应用、排程和商品，以及生成和导出各种报表。它可以帮助商户的管理员和运营者提高工作效率，满足客户的个性化需求，同时帮助客户优化运营流程和营销策略。

# github 地址

仓库地址：https://github.com/troncell/SensingSite/tree/develop

# 1 数据报表

## 1.1 仪表盘

展示当前用户下店铺、商品、设备、会员、订单、销售额等基础统计数据和近期会员购买频次走势以及设备运行状况走势等信息
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/1.png)

## 1.2 销售报表

（1）sku 信息

sku 信息：显示微商城、云货架等应用里，用户购买过的商品 sku 信息记录。会员信息：购买商品 sku 用户信息及购买记录

（2）销售报表

每个店铺的销售详情

（3）商品排行

商品销售前十和商品被点击次数前十的商品

（4）单品明细

显示所有店铺每一单品的销售记录

（5）店铺信息

在地图上展示所有运营店铺的分布情况，方便进行统筹运营管理

## 1.3 行为报表

通过感应商品，显示拿起次数最多排名前十的商品，并展示所有商品 sku 拿起次数、购买次数及销售金额

![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/2.png)

## 1.4 页面统计

获取页面 log 信息
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/3.png)

## 1.5 掉货历史

派样机掉货记录
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/4.png)

## 1.6 客流报表

某个区域每月或每天的客流量报表
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/5.png)

## 1.7 行为分析

商品、筛选、品牌埋点数据统计
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/6.png)

# 2 设备

| 模块                                                                                                         | 描述                                                                                                                                                                 |  |
| ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | - |
| 设备列表                                                                                                     | 支持创建、编辑、删除设备，支持将设备分配到指定店铺，支持设备上下线、删除等操作                                                                                       |  |
| 基础信息                                                                                                     | 管理设备信息，支持对设备进行编辑                                                                                                                                     |  |
| 广告管理                                                                                                     | 支持对带有显示屏的设备进行广告下发，从而进行广告的播放管理，可以添加或撤回广告播放                                                                                   |  |
| 应用管理                                                                                                     | 支持将应用程序下发给支持应用程序运行的设备，通过 AppPod 对应用程序的开启和关闭进行控制和远程管理                                                                     |  |
| 商品管理                                                                                                     | 支持将系统的商品发布给设备，通过创思产品：云货架等以多种不同特效方式进行展示                                                                                         |  |
| 红包管理                                                                                                     | 支持将红包下发给设备，通过游戏、活动页面宣传页等多种途径进行红包派发，用户通过微信或淘宝等进行扫码即可领取                                                           |  |
| 活动管理                                                                                                     | 支持将活动下发给设备，通过在设备上活动页面展示活动二维码吸引用户参与活动（如游戏、派样等）达到吸粉等目的，活动支持微信和淘宝链路，活动结束后系统自动统计活动相关数据 |  |
| 控制                                                                                                         | 控制 apppod,可立即更新获取数据，远程控制设备并且支持批量控制多个设备                                                                                                 |  |
| 数据统计                                                                                                     | 支持接入传感器（温湿度、PM2.5 等多种）、客流摄像头等设备进行相应的数据采集，并以数据报表形式将数据进行展示                                                           |  |
| 第三方信息                                                                                                   | 支持将设备注册淘宝智慧门店或数字门店，完成设备与淘宝链路打通                                                                                                         |  |
| 排程                                                                                                         | 支持将排程发布给设备，通过在设备上展示广告画面，起到宣传效果                                                                                                         |  |
| 货道管理                                                                                                     | 用于派样机，构建货架，给货架配置对应的奖品及库存                                                                                                                     |  |
| 设备审核                                                                                                     | 支持开启和关闭设备审核功能，当开启设备审核时，设备上下线、发布等动作需要管理员审核才生效                                                                             |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/7.png) |                                                                                                                                                                      |  |

# 3 店铺管理

## 3.1 实体店铺

| 模块                                                                                                         | 描述                                                                                                   |  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | - |
| 店铺列表                                                                                                     | 对当前运营的所有店铺进行统一管理，支持添加、编辑和删除店铺、设置店铺上下线状态，将店铺分配到指定的组织 |  |
| 基础信息                                                                                                     | 店铺的信息管理                                                                                         |  |
| 设备管理                                                                                                     | 支持管理当前店铺投放的设备                                                                             |  |
| 广告管理                                                                                                     | 支持管理当前店铺投放的广告                                                                             |  |
| 商品管理                                                                                                     | 支持管理当前店铺销售的商品                                                                             |  |
| 红包管理                                                                                                     | 支持管理当前店铺的优惠红包信息                                                                         |  |
| KPI 管理                                                                                                     | 支持给店铺设置 KPI，并跟踪店铺 KPI 完成情况                                                            |  |
| 库存                                                                                                         | 店铺下的商品库存，可以单个添加或批量添加库存，显示出入库记录                                           |  |
| 房间                                                                                                         | 用于商场导视图里，给店铺绑定或解绑对应房间                                                             |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/8.png) |                                                                                                        |  |

## 3.2 线上店铺

| 模块                                                                                                         | 描述                                                                                                                                       |  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | - |
| 淘宝店铺                                                                                                     | 支持接入淘宝智慧门店和数字门店授权，通过授权后可以从淘宝店铺同步商品到本系统，也可将本系统商品同步到淘宝店铺，支持创建自定义的商品同步计划 |  |
| 微盟店铺                                                                                                     | 支持接入微盟店铺授权，通过授权后可以从微盟店铺同步商品到本系统，也可将本系统商品同步到微盟店铺，支持创建自定义的商品同步计划               |  |
| 微信商城                                                                                                     | 支持创建微信商城，接入创思微信商城系统将商品在微信渠道进行推广销售，支持配置会员等级、积分等规则，支持积分商城功能                         |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/9.png) |                                                                                                                                            |  |

# 4 订单

包含所有订单的支付记录、订单详情以及可对订单进行相关操作
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/10.png)

# 5 会员管理

| 模块                                                                                                          | 描述                                                                                         |  |
| ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | - |
| 会员列表                                                                                                      | 支持查看会员基本信息，对会员信息进行导出、新增、修改和删除等，同时可以对会员等级进行调整管理 |  |
| 积分管理                                                                                                      | 支持查看会员当前积分余额以及会员积分变动记录，可对会员发放积分                               |  |
| 用户反馈                                                                                                      | 收集用户反馈信息及处理状态                                                                   |  |
| 用户预约                                                                                                      | 用户预约信息记录                                                                             |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/11.png) |                                                                                              |  |

# 6 广告

## 6.1 广告列表

| 模块                                                                                                          | 描述                                                                                                                                                 |  |
| ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | - |
| 基础信息                                                                                                      | 支持查看已经创建的广告信息、对广告信息进行导入、新增、修改和删除等操作，支持上传图片、视频、链接等多种类型广告资源，支持对广告进行上下线等操作       |  |
| 自定义广告                                                                                                    | 支持用户创建自定义广告，可自定义广告布局大小，添加图片、视频、二维码、文字、点击热区、轮播图等控件，自定义广告创建后可使用创思信发系统客户端进行播放 |  |
| 广告发布                                                                                                      | 支持将广告发布到对应组织、店铺和设备，使组织、店铺和设备拥有该广告资源                                                                               |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/12.png) |                                                                                                                                                      |  |

## 6.2 广告分组

支持将多个广告放在一个分组中，支持添加点位广告，定义每个广告播放的时长、播放顺序、切换方式等，可以对广告分组进行新增、修改和删除等操作
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/13.png)

# 7 应用管理

| 模块                                                                                                          | 描述                                                                                               |  |
| ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | - |
| 应用列表                                                                                                      | 支持查看当前账户已经有的应用，支持将应用下发到指定组织、店铺和设备，使组织、店铺和设备拥有应用资源 |  |
| 应用中心                                                                                                      | 支持查看应用仓库中展示给租户的所有应用资源，查看应用详细信息，对于需要的应用，可以申请接入         |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/14.png) |                                                                                                    |  |

# 8 排程

## 8.1 24H 节目单

支持将多个广告分组放在节目单，将指定数量的广告分组编排成一个节目单（将多个广告组成一个广告组插入节目单中），进行节目单播放计划管理，支持按日循环、周循环、月循环和特定日期时间进行播放等

![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/15.png)

## 8.2 节目排程

支持将多个广告节目单存入广告排程中，设置排程播放时间
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/16.png)

# 9 导视

楼层管理：支持商场导视图，创建楼、楼层和房间，房间可以绑定店铺和品牌
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/17.png)

# 10 商品

## 10.1 商品列表

| 模块                                                                                                          | 描述                                                                                                                   |  |
| ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | - |
| 基础信息                                                                                                      | 支持查看商品基础信息，支持导入、新增、编辑和删除商品，支持将商品进行上下线操作，支持将商品进行分类和设置标签、绑定品牌 |  |
| 电商平台                                                                                                      | 支持对商品所在电商平台进行管理，配置电商平台访问链接，线下用户扫描商品二维码时可将用户引导到对应电商平台商品详情页     |  |
| SKU 管理                                                                                                      | 支持管理商品下的 SKU 信息，对 SKU 进行新增、修改和删除等操作，支持对 SKU 进行上下限操作，管理 SKU 的图片和视频资源     |  |
| 资源管理                                                                                                      | 支持对商品的资源进行管理，支持管理商品主图、详情图、宣传活动 banner、视频等资源                                        |  |
| 评价管理                                                                                                      | 支持对商品评价进行管理，可以添加、编辑和删除评价                                                                       |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/20.png) |                                                                                                                        |  |

## 10.2 商品属性

支持添加商品属性值，将属性绑定给商品，支持商品多属性并存
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/21.png)

## 10.3 商品分类

支持对商品分类进行管理，支持多级分类
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/22.png)

## 10.4 猜你喜欢

支持添加商品猜你喜欢规则，当用户查看指定商品时，系统自动根据猜你喜欢规则向用户推荐规则中的商品（一般为同类商品）
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/23.png)

## 10.5 定制搭配

支持添加商品搭配规则，当用户查看指定商品时，系统自动根据搭配规则向用户推荐与该商品可形成搭配的相关商品
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/24.png)

## 10.6 促销管理

创建促销活动商品，支持全店促销和单独促销，支持新增、编辑和删除促销
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/25.png)

# 11 品牌管理

## 11.1 品牌中心

支持对商品品牌进行管理，添加多个商品品牌，并将品牌与商品进行绑定，支持商品品牌上下线操作
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/18.png)

## 11.2 品牌分类

支持对品牌分类进行管理，支持多级分类
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/19.png)

# 12 推荐

## 12.1 个性推荐

| 模块                                                                                                          | 描述                                                                                                         |  |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | - |
| 个性推荐                                                                                                      | 支持导入、新增、修改、删除个性信息，个性信息是用户自定义的相关信息，如水瓶座、处女座等相关信息               |  |
| 运势信息                                                                                                      | 支持对个性信息添加运势，根据运势的属性给不同的运势添加不同的商品推荐，从而实现根据用户运势给用户推荐相应商品 |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/26.png) |                                                                                                              |  |

## 12.2 个性分类

支持添加自定义个性推荐分类，如星座、节气、占卜等
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/27.png)

## 12.3 人脸推荐

支持添加人脸标签，并将人脸标签与推荐商品进行绑定，系统获取人脸信息后与人脸标签进行比对之后给对应的人脸推荐相关的商品
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/28.png)

# 13 答题

## 13.1 题库管理

支持创建、编辑、删除试题，将创建的试题发布给试卷，支持试题上下线等操作
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/29.png)

## 13.2 试卷管理

试卷里添加多个试题，组成问卷，支持创建、编辑、删除、上下线试题，试题可以发布到应用，可用于答题派样机
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/30.png)

# 14 权益

## 14.1 红包列表

支持创建、编辑、删除红包，红包支持淘宝现金券、优惠券和用户指定的第三方平台优惠券信息，支持将红包下发给设备进行活动发放，支持红包上下线等操作
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/31.png)

## 14.2 优惠券

| 模块                                                                                                          | 描述                                                                                                                                                                                                       |  |
| ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | - |
| 优惠券创建                                                                                                    | 支持创建当前系统线上（微信商城）线下（实体店）使用的优惠券，优惠券支持抵用券和折扣券两种类型，支持设置优惠券使用条件，如满减、首次购物等，可指定使用的人群、商品、时间等，可设置发券总数和单用户领取次数等 |  |
| 优惠券发放                                                                                                    | 支持指定优惠券领取规则，包括允许用户领取、管理员发放、游戏发放和注册发放等多种规则，同时对于自动发放的优惠券可指定自动发放规则                                                                             |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/32.png) |                                                                                                                                                                                                            |  |

# 15.活动

## 15.1 活动列表

| 模块                                                                                                          | 描述                                                                                                                                   |  |
| ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | - |
| 基础信息                                                                                                      | 支持创建、修改、删除活动信息，支持设置活动相关介绍信息，配置注册和签到等流程，支持将活动上下线，支持将活动发布到指定设备进行活动开展   |  |
| 奖项管理                                                                                                      | 支持给活动配置相关奖项，当用户参与活动达到指定条件即可获得相应奖品                                                                     |  |
| 内容管理                                                                                                      | 支持配置活动的实际内容，包括游戏、抽奖、投票、派样等应用内容，完成与用户的互动过程，并记录用户全部动作，如注册、签到、参与、中奖等数据 |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/33.png) |                                                                                                                                        |  |

## 15.2 数据统计

支持对活动进行数据统计，包括用户注册数据、用户互动数据、奖品发放数据等
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/34.png)

## 15.3 页面模板

支持创建标准活动页面模板，在新建活动时可套用页面模板
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/35.png)

# 16.支付中心

| 模块                                                                                                          | 描述                         |  |
| ------------------------------------------------------------------------------------------------------------- | ---------------------------- | - |
| 支付中心                                                                                                      | 支持添加、编辑、删除支付方式 |  |
| 支付记录                                                                                                      | 显示所有付款记录             |  |
| ![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/36.png) |                              |  |

# 17.系统

## 17.1 标签管理

支持创建不同分类标签，如商品标签、广告标签等，并将标签绑定给对应的商品或者广告，从而实现快速分组、快速检索等
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/37.png)

## 17.2 资源管理

所有资源信息，支持创建、编辑、删除资源，支持给资源设置标签
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/38.png)

## 17.3 公众号/小程序管理

公众号授权 支持快速添加微信公众号/小程序授权，公众号/小程序管理员通过扫描授权二维码即可快速进行公众号/小程序授权，安全便捷
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/39.png)

## 17.4 组织机构

支持添加多级组织机构，支持将用户绑定给对应组织机构，当用户绑定到对应组织后，用户将拥有该组织下所有的权限以及资源的管理权限
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/40.png)

## 17.5 角色管理

支持创建多种不同权限角色，创建用户时将角色配置给用户，用户即可获得当前角色拥有的全部权限
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/41.png)

## 17.6 用户管理

支持添加多个用户，不同用户拥有不同角色权限，分功管理
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/42.png)

## 17.7 语言管理

系统支持多语言切换，包括英语、日语、简体和繁体中文等
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/43.png)

## 17.8 外观设置

支持用户切换系统主体色调

![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/44.png)

## 17.9 基本设置

支持用户编辑公司 logo 等信息
![images](https://sensingstore.oss-cn-shanghai.aliyuncs.com/Troncell/Knowledge/Docs/SensingStore/images/45.png)
