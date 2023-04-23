# Sample介绍
接入不同厂家的贩卖机设备，连通SensingStoreCloud平台，获取货道信息、活动内容、货道库存等信息数据。在贩卖机设备上安装Sample应用，展示活动内容，用户可参与活动，领取贩卖机上的样品。补货人员可定期对派样机进行补货。
# 使用环境
贩卖机设备目前仅支持Android
  | 系统版本 | NAS地址| 
|---|---|
|Android |/产品发布/Release/AppPod/Android|

# github仓库地址：

  Sample：https://github.com/troncell/AppPodAndroid/
  前端地址：https://github.com/troncell/H5Pages/tree/main/sampling
# 使用流程
1. 后台配置：进入[ai.SensingStore.com](https://ai.sensingstore.com/)后台，登录租户，配置派样机活动相关信息，包含模块：设备、线上店铺（微商城）、答题、活动、权益等。

    后台配置说明请参考: [后台配置](https://github.com/troncell/SensingDocs/blob/main/Docs/Sample/%E5%90%8E%E5%8F%B0%E9%85%8D%E7%BD%AE.md)

2. H5页面配置：包含大屏和手机端显示内容的配置

   （1）答题派样：配置首页、答题、答题成功等页面

    详细配置说明请参考:[答题派样页面配置](https://github.com/troncell/SensingDocs/blob/main/Docs/Sample/%E7%AD%94%E9%A2%98%E6%B4%BE%E6%A0%B7%E9%A1%B5%E9%9D%A2%E9%85%8D%E7%BD%AE.md)

   （2）自助售卖派样：配置商品、购买等页面
    详细配置说明请参考:[自助售卖](https://github.com/troncell/SensingDocs/blob/main/Docs/Sample/%E8%87%AA%E5%8A%A9%E5%94%AE%E5%8D%96.md)

3. 设备安装：设备上安装Sample软件。输入服务器地址和设备密钥，调试串口设备，定期对贩卖机进行补货。
  
   详细安装说明请参考：[设备安装](https://github.com/troncell/SensingDocs/blob/main/Docs/Sample/%E8%AE%BE%E5%A4%87%E5%AE%89%E8%A3%85.md)

