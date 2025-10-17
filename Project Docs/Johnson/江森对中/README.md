# 轴对中以及轴间距检测介绍

非接触式激光对中设备，对中设备为瑞典产品，测距设备为日本产品，均为行业头部，精准稳定 厂家出品蓝牙连接 精度高 可精确到 0.01mm 专用工业 PAD（防摔）便携性高，方便操作 使用原生平台开发，使用 wifi 传输字段信息而非传图有后台系统可以记录测量值，测量时间，操作人 ID，方便回溯，保留接口对接能力，可对接公司 MES 等系统，可延展性高。

项目信息文件 NAS 地址：\\192.168.3.8\实施交付\2023 项目交付备份\2023.7.17 江森自控对中

# 使用环境

| 名称         | 部署地址             | 江森访问地址                                                                |
| ------------ | -------------------- | --------------------------------------------------------------------------- |
| hub 前端     | 服务器：10.111.32.23 | 后台访问地址：http://10.111.32.23:8848<br />用户名：admin<br />密码：123qwe |
| hub 后端     | 服务器：10.111.32.23 | http://10.111.32.23:8080/swagger/index.html                                 |
| 大屏         |                      |                                                                             |
| 对中操作系统 | Andriod 平板         |                                                                             |

# github 仓库地址

| 名称     | 说明             | 地址                                                                         | 部署                  | 静态资源 |
| -------- | ---------------- | ---------------------------------------------------------------------------- | --------------------- | -------- |
| hub 前端 | vue3 + vite + ts | https://github.com/troncell/sensinghub_front/tree/centering-data             | 本地 nginx 部署       | 无       |
| 大屏     | vue3 + vite      | https://github.com/troncell/Projects-2023/tree/main/2023/jiangsen/dataScreen | electron 打包，本地部 |          |
| 操作系统 | Andriod          | https://github.com/troncell/Sensing.Test.Centering                           | APK                   |          |

# 使用手册

1.后台环境部署

说明请参考：[江森后台部署文档](https://github.com/troncell/SensingDocs/blob/main/Docs/Centering/%E6%B1%9F%E6%A3%AE%E5%90%8E%E5%8F%B0%E9%83%A8%E7%BD%B2%E6%96%87%E6%A1%A3.md)

2.对中操作说明

说明请参考：[对中操作文档](https://github.com/troncell/SensingDocs/blob/main/Docs/Centering/%E5%AF%B9%E4%B8%AD%E6%93%8D%E4%BD%9C%E6%96%87%E6%A1%A3.md)
