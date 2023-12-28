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

> 维护者为`函数计算`的层，可以直接在函数计算控制台的`添加官方公共层`获取；
> 维护者不是`函数计算`的层，需要通过`层ARN`的方式添加。

### 运行时及其依赖库

| 层名称                          | ARN                                                                       | 说明                                                       | 兼容运行时  | 版本                                                                     | 维护者 |
|------------------------------|---------------------------------------------------------------------------|----------------------------------------------------------|--------|------------------------------------------------------------------------|-----|
| Python310                    | `acs:fc:{region}:official:layers/Python310/versions/2`                    | [README.md](docs/Python310/README.md)                    | `custom`,`custom.debian10`  | Python 3.10.5                                                          | 函数计算 |
| Python310-Package-Collection | `acs:fc:{region}:official:layers/Python310-Package-Collection/versions/2` | [README.md](docs/Python310-Package-Collection/README.md) | `custom`,`custom.debian10`  | [requirements.txt](docs/Python310-Package-Collection/requirements.txt) | 函数计算|
| Python39                     | `acs:fc:{region}:official:layers/Python39/versions/2`                     | [README.md](docs/Python39/README.md)                     | `custom`,`custom.debian10`  | Python 3.9.13                                                          | 函数计算 |
| Python39-Package-Collection  | `acs:fc:{region}:official:layers/Python39-Package-Collection/versions/2`  | [README.md](docs/Python39-Package-Collection/README.md)  | `custom`,`custom.debian10`  | [requirements.txt](docs/Python39-Package-Collection/requirements.txt)  | 函数计算|
| Python38                     | `acs:fc:{region}:official:layers/Python38/versions/2`                     | [README.md](docs/Python38/README.md)                     | `custom`,`custom.debian10`  | Python 3.8.13                                                          | 函数计算 |
| Python38-Package-Collection  | `acs:fc:{region}:official:layers/Python38-Package-Collection/versions/2`  | [README.md](docs/Python38-Package-Collection/README.md)  | `custom`,`custom.debian10`  | [requirements.txt](docs/Python38-Package-Collection/requirements.txt)  | 函数计算|
| Python36                     | `acs:fc:{region}:official:layers/Python36/versions/2`                     | [README.md](docs/Python36/README.md)                     | `custom`  | Python 3.6.15                                                          | 函数计算 |
| Python36-Package-Collection  | `acs:fc:{region}:official:layers/Python36-Package-Collection/versions/2`  | [README.md](docs/Python36-Package-Collection/README.md)  | `custom`  | [requirements.txt](docs/Python36-Package-Collection/requirements.txt)  | 函数计算|
| Dotnet6                      | `acs:fc:{region}:official:layers/Dotnet6/versions/2`                      | [README.md](docs/Dotnet6/README.md)                      | `custom`  | ASP.NET Core Runtime 6.0.5                                             | 函数计算 |
| PHP81                        | `acs:fc:{region}:official:layers/PHP81/versions/5`                        | [README.md](docs/PHP81/README.md)                        | `custom`  | PHP 8.1.9                                                              | 函数计算 |
| PHP80                        | `acs:fc:{region}:official:layers/PHP80/versions/5`                        | [README.md](docs/PHP80/README.md)                        | `custom`  | PHP 8.0.22                                                             | 函数计算 |
| PHP72                        | `acs:fc:{region}:official:layers/PHP72/versions/4`                        | [README.md](docs/PHP72/README.md)                        | `custom`  | PHP 7.2.8                                                              | 函数计算 |
| Java8                       | `acs:fc:{region}:official:layers/Java8/versions/1`                       | [README.md](docs/Java8/README.md)                       | `custom.debian10`  | openjdk 1.8.0_322                                                       | 函数计算 |
| Java11                       | `acs:fc:{region}:official:layers/Java11/versions/2`                       | [README.md](docs/Java11/README.md)                       | `custom`  | openjdk 11.0.13                                                        | 函数计算 |
| Java17                       | `acs:fc:{region}:official:layers/Java17/versions/2`                       | [README.md](docs/Java17/README.md)                       | `custom`  | openjdk 17.0.2                                                         | 函数计算 |
| Nodejs18                     | `acs:fc:{region}:official:layers/Nodejs18/versions/3`                     | [README.md](docs/Nodejs18/README.md)                     | `custom.debian10`  | Node.js 18.19.0                                                         | 函数计算 |
| Nodejs17                     | `acs:fc:{region}:official:layers/Nodejs17/versions/2`                     | [README.md](docs/Nodejs17/README.md)                     | `custom`  | Node.js 17.9.1                                                         | 函数计算 |
| Nodejs16                     | `acs:fc:{region}:official:layers/Nodejs16/versions/2`                     | [README.md](docs/Nodejs16/README.md)                     | `custom`</br>`custom.debian10`  | Node.js 16.17.0                                                        | 函数计算 |
| Nodejs14                     | `acs:fc:{region}:official:layers/Nodejs14/versions/2`                     | [README.md](docs/Nodejs14/README.md)                     | `custom`  | Node.js 14.20.0                                                        | 函数计算 |
| Nodejs12                     | `acs:fc:{region}:official:layers/Nodejs12/versions/2`                     | [README.md](docs/Nodejs12/README.md)                     | `custom`  | Node.js 12.22.12                                                       | 函数计算 |
| Go118                        | `acs:fc:{region}:official:layers/Go118/versions/1`                        | [README.md](docs/Go118/README.md)                        | `custom`  | Go 1.18.8                                                              | 函数计算 |

### 常用依赖库

| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 维护者 |
|---------|------|------|--------|-----| ------------ |
| Python39-Pandas1x | `acs:fc:{region}:official:layers/Python39-Pandas1x/versions/2` | [README.md](docs/Python39-Pandas1x/README.md) | `python3.9`</br>`custom`</br>`custom.debian10`  | pandas-1.4.3 | 函数计算 |
| Python39-SciPy1x | `acs:fc:{region}:official:layers/Python39-SciPy1x/versions/2` | [README.md](docs/Python39-SciPy1x/README.md) | `python3.9`</br>`custom`  | scipy-1.9.0</br>numpy-1.23.2 | 函数计算 |
| Python36-SciPy1x | `acs:fc:{region}:official:layers/Python36-SciPy1x/versions/4` | [README.md](docs/Python36-SciPy1x/README.md) | `python3.6`</br>`custom`  | scipy-1.5.4</br>numpy-1.19.5 | 函数计算 |
| Python39-PyTorch1x | `acs:fc:{region}:official:layers/Python39-PyTorch1x/versions/2` | [README.md](docs/Python39-PyTorch1x/README.md) | `python3.9`</br>`custom`</br>`custom.debian10`  | torch-1.12.1+cpu</br>torchaudio-0.12.1+cpu</br>torchvision-0.13.1+cpu | 函数计算 |
| Python36-PyTorch1x | `acs:fc:{region}:official:layers/Python36-PyTorch1x/versions/2` | [README.md](docs/Python36-PyTorch1x/README.md) | `python3.6`</br>`custom`  | torch-1.10.2+cpu</br>torchvision-0.11.3+cpu</br>torchaudio-0.10.2+cpu | 函数计算 |
| Python3-Flask2x | `acs:fc:{region}:official:layers/Python3-Flask2x/versions/2` | [README.md](docs/Python3-Flask2x/README.md) | `python3.9`</br>`python3.10`</br>`custom`</br>`custom.debian10`  | flask-2.2.2 | 函数计算 |
| Nodejs-Puppeteer17x | `acs:fc:{region}:official:layers/Nodejs-Puppeteer17x/versions/3` | [README.md](docs/Nodejs-Puppeteer17x/README.md) | `nodejs16`</br>`nodejs14`</br>`custom`</br>`custom.debian10`  | puppeteer-v17.1.0 | 函数计算 |
| Nodejs-Puppeteer10x | `acs:fc:{region}:official:layers/Nodejs-Puppeteer10x/versions/2` | [README.md](docs/Nodejs-Puppeteer10x/README.md) | `nodejs14`</br>`nodejs12`</br>`nodejs10`</br>`custom`  | puppeteer-v10.2.0 | 函数计算 |
| Python3-cx_Oracle8x | `acs:fc:{region}:1940309364339785:layers/Python3-cx_Oracle8x/versions/1` | [github.com/fanzhe/fc-layer/python3-cxOracle](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-cxOracle/README.md)) | `python3.9`</br>`python3`</br>`custom`  | cx_Oracle-8.3 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| PuppeteerLib | `acs:fc:{region}:1940309364339785:layers/PuppeteerLib/versions/1` | [github.com/fanzhe/fc-layer/puppeteer-lib](https://github.com/fanzhe328/fc-layer/blob/main/layers/PuppeteerLib/README.md)) | `custom`</br>`nodejs16`</br>`nodejs14`</br>`nodejs12`</br>`nodejs10`</br>`nodejs8`  |  | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python310-Opencv4x | `acs:fc:{region}:official:layers/Python310-Opencv4x/versions/2` | [README.md](docs/Python310-Opencv4x/README.md) | `python3.10`</br>`custom.debian10`  | opencv_python-4.7.0.68 | 函数计算 |
| SQLite3             | `acs:fc:{region}:official:layers/SQLite3/versions/1`      | [README.md](docs/Sqlite3/README.md) | `custom`</br>`python3.9`</br>`nodejs14`</br>`nodejs16`</br>`java8`</br>`java11` | 3.41.1 |      函数计算      |
| FFmpeg6x             | `acs:fc:{region}:official:layers/FFmpeg6x/versions/1`      | [README.md](docs/FFmpeg6x/README.md) | `custom`</br>`custom.debian10`</br>`python3.10`</br>`python3.9`</br>`nodejs14`</br>`nodejs16`</br>`java8`</br>`java11` | 6.0 |      函数计算      |
| Nodejs-Puppeteer19x | `acs:fc:{region}:official:layers/Nodejs-Puppeteer19x/versions/1` | [README.md](docs/Nodejs-Puppeteer19x/README.md) | `custom.debian10`  | puppeteer-v19.8.5 | 函数计算 |
| Python38-Playwright | `acs:fc:{region}:official:layers/Python38-Playwright/versions/1` | [README.md](docs/Python38-Playwright/README.md) | `custom.debian10`  | playwright-v1.31.1 | 函数计算 |
| Poppler22x-Pdf2image | `acs:fc:{region}:official:layers/Poppler22x-Pdf2image/versions/1` | [README.md](docs/Poppler22x-Pdf2image/README.md) | `python3.10`  | pdf2image-1.16.3, poppler-22.12.0 | 函数计算 |
| ServerlessDevs | `acs:fc:{region}:official:layers/ServerlessDevs/versions/2` | [README.md](docs/ServerlessDevs/README.md) | `custom.debian10`,`python3.10`,`custom`,`python3.9`,`python3`,`nodejs16`,`nodejs14`,`java11`,`java8`,`go1`,`dotnetcore3.1`,`php7.2`  | 3.0.0 | 函数计算 |

#### Web 框架

| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 维护者 |
|---------|------|------|--------|-----| ------------ |
| Python3-Flask2x | `acs:fc:{region}:official:layers/Python3-Flask2x/versions/1` | [README.md](docs/Python3-Flask2x/README.md) | `custom`,`python3.9` | flask-2.2.2 | 函数计算 |
| Python3-Bottle | `acs:fc:{region}:1940309364339785:layers/Python3-Bottle/versions/1` | [github.com/fanzhe/fc-layer/python3-bottle](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-bottle/README.md)) | `custom` | bottle-0.12.23 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-Django4x | `acs:fc:{region}:1940309364339785:layers/Python3-Django4x/versions/1` | [github.com/fanzhe/fc-layer/python3-Django4x](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-Django4x/README.md)) | `custom` | Django-4.1.3 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-FastAPI | `acs:fc:{region}:1940309364339785:layers/Python3-FastAPI/versions/1` | [github.com/fanzhe/fc-layer/python3-fastapi](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-fastapi/README.md)) | `custom` | FastAPI-0.86.0 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-Pyramid2x | `acs:fc:{region}:1940309364339785:layers/Python3-Pyramid2x/versions/1` | [github.com/fanzhe/fc-layer/python3-pyramid](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-pyramid/README.md)) | `custom` | Pyramid-2.0 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-Tornado6x | `acs:fc:{region}:1940309364339785:layers/Python3-Tornado6x/versions/1` | [github.com/fanzhe/fc-layer/python3-tornado6x](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-tornado6x/README.md)) | `custom` | tornado-6.2 | [fanzhe](https://github.com/fanzhe328/fc-layer) |
| Python3-WebPy | `acs:fc:{region}:1940309364339785:layers/Python3-WebPy/versions/1` | [github.com/fanzhe/fc-layer/python3-webpy](https://github.com/fanzhe328/fc-layer/blob/main/layers/python3-webpy/README.md)) | `custom` | web.py-0.62 | [fanzhe](https://github.com/fanzhe328/fc-layer) |

### 阿里云 SDK

| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 备注 |
|---------|------|------|--------|-----|---------- |
| Aliyun-DataX | `acs:fc:{region}:official:layers/Aliyun-DataX/versions/2` | 阿里云 DataWorks数据集成的开源版本:[README.md](docs/Aliyun-DataX/README.md) | `python2.7`</br>`python3.6`</br>`python3.9`</br>`python3.10`</br>`custom`</br>`custom.debian10`  | datax_v202210 | 函数计算 |
| Python39-Aliyun-SDK | `acs:fc:{region}:official:layers/Python39-Aliyun-SDK/versions/2` | 阿里云常用 SDK (Python3.9) | `python3.9`</br>`custom`  | | 函数计算 |
| Python36-Aliyun-SDK | `acs:fc:{region}:official:layers/Python36-Aliyun-SDK/versions/2` | 阿里云常用SDK (Python3.6) | `python3.6`</br>`custom`  | | 函数计算 |
| Nodejs-Aliyun-SDK | `acs:fc:{region}:official:layers/Nodejs-Aliyun-SDK/versions/2` | 阿里云常用SDK (Nodejs16/Nodejs14/Nodejs12) | `nodejs16`</br>`nodejs14`</br>`nodejs12`</br>`custom`</br>`custom.debian10`  | | 函数计算 |

### 运行时扩展

| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 备注 |
|---------|------|------|--------|-----|---------- |
| ArmsAgent273x | `acs:fc:{region}:official:layers/ArmsAgent273x/versions/1` | 阿里云应用实时监控服务[ARMS](https://arms.console.aliyun.com/) | `java8`</br>`java11`</br>`custom`</br>`custom.debian10`  | v2.7.3.5 | 函数计算 |
| ArmsAgent273x_JDK17 | `acs:fc:{region}:official:layers/ArmsAgent273x_JDK17/versions/1` | 阿里云应用实时监控服务[ARMS](https://arms.console.aliyun.com/) | `custom`</br>`custom.debian10`  | v2.7.3.5-jdk17 | 函数计算 |
| Loggie13x | `acs:fc:{region}:official:layers/Loggie13x/versions/1` | 云原生日志Agent[Loggie](https://loggie-io.github.io/docs/) | `custom`</br>`custom.debian10`  | v1.3.0 | 函数计算 |

## 参考

- [Custom-Runtime 运行时官方文档](https://help.aliyun.com/document_detail/132042.html)
