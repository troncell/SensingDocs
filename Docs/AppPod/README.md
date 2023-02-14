# AppPod介绍
简介：
支持Windows和Android在显示设备上安装AppPod，登录密钥，获取SensingStoreCloud平台数据，将线上的资源下载至本地，下载后显示设备上播放下载的资源。

特点：

高效发布：只需进行资源上传-下发设备即可快速将影音资料发布到终端。

内容多样：支持主流的视频，图片格式，能播放HTML页面等其它扩展格式并增强富媒体特性。

自由布局：视频、图片可以自由随性的摆放，并且能够适配不同尺寸的显示器

智能排程：可将一组广告排布到时间轴上，按需播放，支持各类循环，自由定义播放时间。

设备管理：支持设备、门店、区域按需发布或者一键全部下发。发布后支持追加更新，撤回前端联网自动及时更新。
# 使用环境
信息发布支持Android和Windows

  | 系统版本  | 版本 | 版本发布时间 | 版本下载链接| NAS地址| 修改内容 |
|---|---|---|---|---|---|---|
|Windows|AppPod-Win-4.0.1.5 | 2022/12/19  | https://troncell-releases.oss-cn-shanghai.aliyuncs.com/AppPod/Windows/AppPod-Win-4.0.1.5.7z|/产品发布/Release/AppPod/Windows | 修改更新云货架后，排程内容不显示|
|Android|V3.1.16 | 2022/2/1 | https://troncell-releases.oss-cn-shanghai.aliyuncs.com/AppPod/Android/sensingads/com.troncell.apppod-v3.1.16-release.apk|/产品发布/Release/AppPod/Android |添加Debug模式:默认关闭Debug模式，下拉web不会刷新；打开Debug模式，下拉web会刷新|
# github仓库地址：

Windows仓库：

Android仓库：https://github.com/troncell/AppPodAndroid
# 使用流程
1. 后台配置：进入[ai.SensingStore.com](https://ai.sensingstore.com/)后台，登录租户，配置播放素材等信息，包含模块：设备、广告、排程等。
   
    后台配置说明请参考：[信息发布](https://github.com/troncell/SensingDocs/blob/main/Docs/AppPod/%E4%BF%A1%E6%81%AF%E5%8F%91%E5%B8%83.md)

1. 软件安装：支持Android和Windows，设备上安装AppPod软件。输入服务器地址和设备密钥，点击注册，设备播放后台创建的素材

   详细安装说明请参考：[AppPod安装](https://github.com/troncell/SensingDocs/blob/main/Docs/AppPod/AppPod%E5%AE%89%E8%A3%85.md)