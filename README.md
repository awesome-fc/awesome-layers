# 阿里云-函数计算-公共层

该项目提供了一些精选的函数计算公共层。
层可以为您提供自定义的公共依赖库、运行时环境及函数扩展等发布与部署能力。您可以直接使用本文列举的公共层，以减少部署、更新时的代码包体积，也可以快速的开发和测试您的代码。

详细信息可参考官方文档

- [构建层](https://help.aliyun.com/document_detail/193057.html)
- [使用层](https://help.aliyun.com/document_detail/193058.html)

## 公共层

公共层主要分为以下几类:

- 运行时及其依赖库
- 常用依赖库
- 阿里云 SDK

> 1. 维护者为`函数计算`的层，可以直接在函数计算控制台的`添加官方公共层`获取；维护者不是`函数计算`的层，需要通过`层ARN`的方式添加。
>
> 2. 官方公共层终止支持后，函数计算不再继续提供对该公共层的版本更新，已终止支持的公共层仍然可以继续使用。但建议您将函数迁移至最新支持的公共层，以便获得技术支持和安全更新。

### 运行时及其依赖库

以下公共层由阿里云函数计算维护。

| 层名称    | ARN/说明      | 兼容运行时  |  终止支持时间(EOF) |
|------------------|-----------------|--------|-----|
| PHP81-Debian10  | `acs:fc:{region}:official:layers/PHP81-Debian10/versions/1`</br>[README.md](docs/PHP81-Debian10/README.md) | `custom.debian10`  | 暂无明确时间 |
| Nginx  | `acs:fc:{region}:official:layers/Nginx/versions/1`</br>[README.md](docs/Nginx/README.md) | `custom.debian10`  | 暂无明确时间 |
| PHP80-Debian10  | `acs:fc:{region}:official:layers/PHP80-Debian10/versions/2`</br>[README.md](docs/PHP80-Debian10/README.md) | `custom.debian10`  | 暂无明确时间 |
| Python310                    | `acs:fc:{region}:official:layers/Python310/versions/2`</br>[README.md](docs/Python310/README.md)     |  `custom`</br>`custom.debian10`  | 暂无明确时间 |
| Python310-Package-Collection | `acs:fc:{region}:official:layers/Python310-Package-Collection/versions/3`</br>[README.md](docs/Python310-Package-Collection/README.md) | `custom.debian10` | 暂无明确时间|
| Python39                     | `acs:fc:{region}:official:layers/Python39/versions/2`</br>[README.md](docs/Python39/README.md)                     | `custom`</br>`custom.debian10` | 暂无明确时间 |
| Python39-Package-Collection  | `acs:fc:{region}:official:layers/Python39-Package-Collection/versions/3`</br>[README.md](docs/Python39-Package-Collection/README.md)  | `custom`</br>`custom.debian10` | 暂无明确时间|
| Python38                     | `acs:fc:{region}:official:layers/Python38/versions/2`</br>[README.md](docs/Python38/README.md)                     | `custom`</br>`custom.debian10`  | 暂无明确时间 |
| Python38-Package-Collection  | `acs:fc:{region}:official:layers/Python38-Package-Collection/versions/2`</br>[README.md](docs/Python38-Package-Collection/README.md)  | `custom`</br>`custom.debian10` | 暂无明确时间|
| Python36                     | `acs:fc:{region}:official:layers/Python36/versions/2`</br>[README.md](docs/Python36/README.md)                     | `custom`  | 2024-04 |
| Python36-Package-Collection  | `acs:fc:{region}:official:layers/Python36-Package-Collection/versions/2`</br>[README.md](docs/Python36-Package-Collection/README.md)  | `custom` | 2024-04 |
| Dotnet6                      | `acs:fc:{region}:official:layers/Dotnet6/versions/2`</br>README.md](docs/Dotnet6/README.md)                      | `custom`  | 暂无明确时间 |
| PHP81                        | `acs:fc:{region}:official:layers/PHP81/versions/6`</br>[README.md](docs/PHP81/README.md)                        | `custom`  | 暂无明确时间 |
| PHP80                        | `acs:fc:{region}:official:layers/PHP80/versions/7`</br>[README.md](docs/PHP80/README.md)                        | `custom`  | 暂无明确时间 |
| PHP72                        | `acs:fc:{region}:official:layers/PHP72/versions/6`</br>[README.md](docs/PHP72/README.md)                        | `custom`  | 暂无明确时间 |
| Java8                       | `acs:fc:{region}:official:layers/Java8/versions/1`</br>[README.md](docs/Java8/README.md)                       | `custom.debian10`| 暂无明确时间 |
| Java11                       | `acs:fc:{region}:official:layers/Java11/versions/2`</br>[README.md](docs/Java11/README.md)                       | `custom`| 暂无明确时间 |
| Java17                       | `acs:fc:{region}:official:layers/Java17/versions/2`</br>[README.md](docs/Java17/README.md)                       | `custom`  | 暂无明确时间 |
| Nodejs20                     | `acs:fc:{region}:official:layers/Nodejs20/versions/1`</br>[README.md](docs/Nodejs20/README.md)                     | `custom.debian10` | 暂无明确时间 |
| Nodejs18                     | `acs:fc:{region}:official:layers/Nodejs18/versions/3`</br>[README.md](docs/Nodejs18/README.md)                     | `custom.debian10` | 暂无明确时间 |
| Nodejs17                     | `acs:fc:{region}:official:layers/Nodejs17/versions/2`</br>[README.md](docs/Nodejs17/README.md)                     | `custom` | 暂无明确时间 |
| Nodejs16                     | `acs:fc:{region}:official:layers/Nodejs16/versions/2`</br>[README.md](docs/Nodejs16/README.md)                     | `custom`</br>`custom.debian10` | 暂无明确时间 |
| Nodejs14                     | `acs:fc:{region}:official:layers/Nodejs14/versions/2`</br>[README.md](docs/Nodejs14/README.md)                     | `custom` | 暂无明确时间 |
| Nodejs12                     | `acs:fc:{region}:official:layers/Nodejs12/versions/2`</br>[README.md](docs/Nodejs12/README.md)                     | `custom`   | 暂无明确时间 |
| Go118                        | `acs:fc:{region}:official:layers/Go118/versions/1`</br>[README.md](docs/Go118/README.md)                        | `custom` | 暂无明确时间 |

### 常用依赖库

以下公共层由阿里云函数计算维护。

| 层名称  | ARN/说明 | 兼容运行时  | 终止支持时间(EOF) | 维护者 |
|---------|------|------|-----|----------|
| Python310-OSS2 | `acs:fc:{region}:official:layers/Python310-OSS2/versions/1`</br>[README.md](docs/Python310-OSS2/README.md) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python39-OSS2 | `acs:fc:{region}:official:layers/Python39-OSS2/versions/1`</br>[README.md](docs/Python39-OSS2/README.md) | `python3.9`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python310-TensorFlow2x | `acs:fc:{region}:official:layers/Python310-TensorFlow2x/versions/1`</br>[README.md](docs/Python310-TensorFlow2x/README.md) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python3x-PyMongo4x | `acs:fc:{region}:official:layers/Python3x-PyMongo4x/versions/1`</br>[README.md](docs/Python3x-PyMongo4x/README.md) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python3x-Pandas2x | `acs:fc:{region}:official:layers/Python3x-Pandas2x/versions/1`</br>[README.md](docs/Python3x-Pandas2x/README.md) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python310-PyTorch2x | `acs:fc:{region}:official:layers/Python310-PyTorch2x/versions/1`</br>[README.md](docs/Python310-PyTorch2x/README.md) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python39-Pandas1x | `acs:fc:{region}:official:layers/Python39-Pandas1x/versions/2`</br>[README.md](docs/Python39-Pandas1x/README.md) | `python3.9`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python39-SciPy1x | `acs:fc:{region}:official:layers/Python39-SciPy1x/versions/2`</br>[README.md](docs/Python39-SciPy1x/README.md) | `python3.9`</br>`custom`  | 暂无明确时间 | 函数计算 |
| Python36-SciPy1x | `acs:fc:{region}:official:layers/Python36-SciPy1x/versions/4`</br>[README.md](docs/Python36-SciPy1x/README.md) | `python3.6`</br>`custom`  | 2024-04 | 函数计算 |
| Python39-PyTorch1x | `acs:fc:{region}:official:layers/Python39-PyTorch1x/versions/2`</br>[README.md](docs/Python39-PyTorch1x/README.md) | `python3.9`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python36-PyTorch1x | `acs:fc:{region}:official:layers/Python36-PyTorch1x/versions/2`</br>[README.md](docs/Python36-PyTorch1x/README.md) | `python3.6`</br>`custom`  | 2024-04 | 函数计算 |
| Python3-Flask2x | `acs:fc:{region}:official:layers/Python3-Flask2x/versions/2`</br>[README.md](docs/Python3-Flask2x/README.md) | `python3.9`</br>`python3.10`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Nodejs-Puppeteer17x | `acs:fc:{region}:official:layers/Nodejs-Puppeteer17x/versions/3`</br>[README.md](docs/Nodejs-Puppeteer17x/README.md) | `nodejs16`</br>`nodejs14`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Nodejs-Puppeteer10x | `acs:fc:{region}:official:layers/Nodejs-Puppeteer10x/versions/2`</br>[README.md](docs/Nodejs-Puppeteer10x/README.md) | `nodejs14`</br>`nodejs12`</br>`nodejs10`</br>`custom`  | 2024-04 | 函数计算 |
| Python3-cx_Oracle8x | `acs:fc:{region}:1940309364339785:layers/Python3-cx_Oracle8x/versions/1`</br>[github.com/fanzhe/fc-layer/python3-cxOracle](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-cxOracle/README.md)) | `python3.9`</br>`python3`</br>`custom`  | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| PuppeteerLib | `acs:fc:{region}:1940309364339785:layers/PuppeteerLib/versions/1`</br>[github.com/fanzhe/fc-layer/puppeteer-lib](https://github.com/fanzhe328/fc-layer/blob/main/layers/PuppeteerLib/README.md)) | `custom`</br>`nodejs16`</br>`nodejs14`</br>`nodejs12`</br>`nodejs10`</br>`nodejs8`  | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python310-Opencv4x | `acs:fc:{region}:official:layers/Python310-Opencv4x/versions/2`</br>[README.md](docs/Python310-Opencv4x/README.md) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| SQLite3             | `acs:fc:{region}:official:layers/SQLite3/versions/1`</br>[README.md](docs/Sqlite3/README.md) | `custom`</br>`python3.9`</br>`nodejs14`</br>`nodejs16`</br>`java8`</br>`java11` | 暂无明确时间 |      函数计算      |
| FFmpeg6x             | `acs:fc:{region}:official:layers/FFmpeg6x/versions/1`</br>[README.md](docs/FFmpeg6x/README.md) | `custom`</br>`custom.debian10`</br>`python3.10`</br>`python3.9`</br>`nodejs14`</br>`nodejs16`</br>`java8`</br>`java11` | 暂无明确时间 |      函数计算      |
| Nodejs-Puppeteer19x | `acs:fc:{region}:official:layers/Nodejs-Puppeteer19x/versions/1`</br>[README.md](docs/Nodejs-Puppeteer19x/README.md) | `custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python38-Playwright | `acs:fc:{region}:official:layers/Python38-Playwright/versions/1`</br>[README.md](docs/Python38-Playwright/README.md) | `custom.debian10`  | 暂无明确时间 | 函数计算 |
| Poppler22x-Pdf2image | `acs:fc:{region}:official:layers/Poppler22x-Pdf2image/versions/1`</br>[README.md](docs/Poppler22x-Pdf2image/README.md) | `python3.10`  | 暂无明确时间 | 函数计算 |
| ServerlessDevs | `acs:fc:{region}:official:layers/ServerlessDevs/versions/2`</br>[README.md](docs/ServerlessDevs/README.md) | `custom.debian10`</br>`python3.10`</br>`custom`</br>`python3.9`</br>`python3`</br>`nodejs16`</br>`nodejs14`</br>`java11`</br>`java8`</br>`go1`</br>`dotnetcore3.1`</br>`php7.2`</br> | 暂无明确时间 | 函数计算 |

以下公共层由开发者维护。

| 层名称  | ARN/说明 | 兼容运行时  | 终止支持时间(EOF) | 维护者 |
|---------|------|------|-----|----------|
| Python3x-PyMongo4x | `acs:fc:{region}:1730431480417716:layers/Python3x-PyMongo4x/versions/1`</br>版本: pymongo==4.6.1 | `custom.debian10`</br>`python3.10`</br>`python3.9` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |

#### Web 框架

| 层名称  | ARN/说明 | 兼容运行时  | 终止支持时间(EOF) | 维护者 |
|---------|------|------|-----|---------|
| Python3-Flask2x | `acs:fc:{region}:official:layers/Python3-Flask2x/versions/1`</br>[README.md](docs/Python3-Flask2x/README.md) | `custom`,`python3.9` | 暂无明确时间 | 函数计算 |
| Python3-Bottle | `acs:fc:{region}:1940309364339785:layers/Python3-Bottle/versions/1`</br>[github.com/fanzhe/fc-layer/python3-bottle](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-bottle/README.md)) | `custom` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-Django4x | `acs:fc:{region}:1940309364339785:layers/Python3-Django4x/versions/1`</br>[github.com/fanzhe/fc-layer/python3-Django4x](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-Django4x/README.md)) | `custom` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-FastAPI | `acs:fc:{region}:1940309364339785:layers/Python3-FastAPI/versions/1`</br>[github.com/fanzhe/fc-layer/python3-fastapi](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-fastapi/README.md)) | `custom` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-Pyramid2x | `acs:fc:{region}:1940309364339785:layers/Python3-Pyramid2x/versions/1`</br>[github.com/fanzhe/fc-layer/python3-pyramid](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-pyramid/README.md)) | `custom` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-Tornado6x | `acs:fc:{region}:1940309364339785:layers/Python3-Tornado6x/versions/1`</br>[github.com/fanzhe/fc-layer/python3-tornado6x](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-tornado6x/README.md)) | `custom` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-WebPy | `acs:fc:{region}:1940309364339785:layers/Python3-WebPy/versions/1`</br>[github.com/fanzhe/fc-layer/python3-webpy](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-webpy/README.md)) | `custom` | 暂无明确时间 | [fanzhe](https://github.com/fanzhe328/fc-layer) |

### 阿里云 SDK

| 层名称  | ARN/说明 | 兼容运行时  | 终止支持时间(EOF) | 维护者 |
|---------|------|--------|-----|-------|
| Python310-Aliyun-SDK | `acs:fc:{region}:official:layers/Python310-Aliyun-SDK/versions/1`</br>阿里云常用 SDK (Python3.10) | `python3.10`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Aliyun-DataX | `acs:fc:{region}:official:layers/Aliyun-DataX/versions/2`</br>阿里云 DataWorks数据集成的开源版本(datax_v202210):[README.md](docs/Aliyun-DataX/README.md)  | `python2.7`</br>`python3.6`</br>`python3.9`</br>`python3.10`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Python39-Aliyun-SDK | `acs:fc:{region}:official:layers/Python39-Aliyun-SDK/versions/2`</br>阿里云常用 SDK (Python3.9) | `python3.9`</br>`custom`  | 暂无明确时间 | 函数计算 |
| Python36-Aliyun-SDK | `acs:fc:{region}:official:layers/Python36-Aliyun-SDK/versions/2`</br>阿里云常用SDK (Python3.6) | `python3.6`</br>`custom`  | 2024-04 | 函数计算 |
| Nodejs-Aliyun-SDK | `acs:fc:{region}:official:layers/Nodejs-Aliyun-SDK/versions/3`</br>阿里云常用SDK | `nodejs20`</br>`nodejs18`</br>`nodejs16`</br>`nodejs14`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |

### 运行时扩展

| 层名称  | ARN/说明 | 兼容运行时  | 终止支持时间(EOF) | 维护者 |
|---------|------|--------|-----|--------|
| ArmsAgent273x | `acs:fc:{region}:official:layers/ArmsAgent273x/versions/1`</br>阿里云应用实时监控服务[ARMS-v2.7.3.5](https://arms.console.aliyun.com/) | `java8`</br>`java11`</br>`custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| ArmsAgent273x_JDK17 | `acs:fc:{region}:official:layers/ArmsAgent273x_JDK17/versions/1`</br>阿里云应用实时监控服务[ARMS-v2.7.3.5-jdk17](https://arms.console.aliyun.com/) | `custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |
| Loggie13x | `acs:fc:{region}:official:layers/Loggie13x/versions/1`</br>云原生日志Agent[Loggie](https://loggie-io.github.io/docs/) | `custom`</br>`custom.debian10`  | 暂无明确时间 | 函数计算 |

## 参考

- [Custom-Runtime 运行时官方文档](https://help.aliyun.com/document_detail/132042.html)
