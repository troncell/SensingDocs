# 人店介绍

人脸闸门：无人店能够识别会员身份。用户 ID 与进闸机时的面部识别信息或者和会员二维码进行绑定，绑定后可通过刷脸或者刷码进入无人店

感应货架：连接 sensingstore 平台，货道绑定商品和发射器，实时检测商品拿起行为，识别用户取货

电子价签：是一种带有收发信息功能的电子显示装置，电子价签放置在货架上，可替代传统纸质价格标签，可修改商品信息实时显示

条形屏：接收到商品拿起行为后，条形屏展示拿起商品信息

无人店小程序（Unmanned Store Mini-program）包含用户端和营业员端。用户端需要开通微信支付分，支付分达到一定的分数可生成入店二维码。用户可扫码进店选取商品，出店后，自动生成订单并完成扣费。营业员端可对商品和货架进行管理，以营业员身份入店不会生成订单。

# 使用环境

闸机、条形屏、货架 apk 目前仅支持 Android

# github 仓库地址：

无人店小程序地址：[troncell/CatchGoInStore (github.com)](https://github.com/troncell/CatchGoInStore "https://github.com/troncell/CatchGoInStore")

接口文档地址：https://apifox.com/apidoc/shared-3bcc4ec5-ec7e-42b3-9bc5-a8fdf2483f45

原型图地址：https://modao.cc/app/nVzWeqtis54ceuR9lRgFL #无人店-分享

流程图地址：https://js.design/f/2G_g9N?p=57aTbdvBMf&mode=design

# 使用流程

1. 闸机 apk 安装，配置说明请参考：[闸机 apk 安装](https://github.com/troncell/SensingDocs/blob/main/Docs/UnmannedShop/%E9%97%B8%E6%9C%BAapk%E5%AE%89%E8%A3%85.md)
2. 货架校准，配置说明请参考：[货架校准](https://github.com/troncell/SensingDocs/blob/main/Docs/UnmannedShop/%E8%B4%A7%E6%9E%B6%E6%A0%A1%E5%87%86.md)
3. 电子价签设置，配置说明请参考：[ElectronicPriceTag 文件](https://github.com/troncell/SensingDocs/tree/main/Docs/ElectronicPriceTag)
4. 后台货架设置，配置说明请参考：[后台操作](https://github.com/troncell/SensingDocs/blob/main/Docs/UnmannedShop/%E5%90%8E%E5%8F%B0%E6%93%8D%E4%BD%9C.md)
5. 货架 apk 安装，配置说明请参考：[安装货架](https://github.com/troncell/SensingDocs/blob/main/Docs/UnmannedShop/%E5%AE%89%E8%A3%85%E8%B4%A7%E6%9E%B6.md)
6. 条形屏 apk 安装，配置说明请参考：[信息发布](https://github.com/troncell/SensingDocs/blob/main/Docs/AppPod/SensingApp%E5%AE%89%E8%A3%85.md)
