# AppPod 介绍

简介：
支持 Windows 和 Android 在显示设备上安装 AppPod，登录密钥，获取 SensingStoreCloud 平台数据，将线上的资源下载至本地，下载后显示设备上播放下载的资源。

特点：

高效发布：只需进行资源上传-下发设备即可快速将影音资料发布到终端。

内容多样：支持主流的视频，图片格式，能播放 HTML 页面等其它扩展格式并增强富媒体特性。

自由布局：视频、图片可以自由随性的摆放，并且能够适配不同尺寸的显示器

智能排程：可将一组广告排布到时间轴上，按需播放，支持各类循环，自由定义播放时间。

设备管理：支持设备、门店、区域按需发布或者一键全部下发。发布后支持追加更新，撤回前端联网自动及时更新。

# 使用环境

信息发布支持 Android 和 Windows

| 系统版本 | 阿里云下载地址                                                                                                       | 钉钉下载             | 版本地址（NAS）                               |
| -------- | -------------------------------------------------------------------------------------------------------------------- | -------------------- | --------------------------------------------- |
| Android  | https://oss.console.aliyun.com/bucket/oss-cn-shanghai/troncell-releases/object?path=AppPod%2FAndroid%2Fsensingads%2F | 钉钉群：创思软件发布 | \\192.168.3.8\产品发布\Release\AppPod\Android |
| Windows  | 无                                                                                                                   | 无                   | \\192.168.3.8\产品发布\Release\AppPod\Windows |

# github 仓库地址：

Windows 仓库：https://github.com/wulixu/AppPod.git

Android 仓库：https://github.com/troncell/AppPodAndroid

接口文档：https://apifox.com/apidoc/shared-0fae02b4-c453-4261-afc4-7d47d2887e5d

# 使用流程

1. 后台配置：进入[ai.SensingStore.com](https://ai.sensingstore.com/)后台，登录租户，配置播放素材等信息，包含模块：设备、广告、排程等。

   后台配置说明请参考：[信息发布](https://github.com/troncell/SensingDocs/blob/main/Docs/AppPod/%E4%BF%A1%E6%81%AF%E5%8F%91%E5%B8%83.md)

2. 软件安装：支持 Android 和 Windows，设备上安装 AppPod 软件。输入服务器地址和设备密钥，点击注册，设备播放后台创建的素材

   详细安装说明请参考：[AppPod 安装](https://github.com/troncell/SensingDocs/blob/main/Docs/AppPod/AppPod%E5%AE%89%E8%A3%85.md)
