
# 【官方公共层】ArmsAgent4x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/ArmsAgent4x/versions/1` | `java8`,`java11`, `custom`,`custom.debian10`,`custom.debian11`   |  v4.1.12  |

阿里云应用实时监控服务[ARMS](https://arms.console.aliyun.com/)。


## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

arms jar 包在zip包的目录 `ArmsAgent/arms-bootstrap-1.7.0-SNAPSHOT.jar`下，在函数计算中会解压到 `/opt` 目录下，在函数计算运行环境内，该jar包在目录 `/opt/ArmsAgent/arms-bootstrap-1.7.0-SNAPSHOT.jar`下。

在java8、java11 运行时中:

1. 配置环境变量 `JAVA_TOOL_OPTIONS=/opt/ArmsAgent/arms-bootstrap-1.7.0-SNAPSHOT.jar`。
2. 设置环境变量 `FC_EXTENSIONS_ARMS_LICENSE_KEY=xxxx` ，值为License Key 信息。关于License Key信息的获取方式，请参见 [获取License Key信息](https://help.aliyun.com/zh/arms/application-monitoring/user-guide/install-the-arms-agent-for-a-java-application-in-function-compute?spm=a2c4g.11186623.0.0.4aef4625AcojfK#arms-cs-k8s-java)。

## License


## 参考信息
维护者：阿里云-函数计算