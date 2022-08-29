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

### 运行时及其依赖库
| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 备注 |
|---------|------|------|--------|-----|-----|
| Python310 | acs:fc:{region}:official:layers/Python310/versions/1 | [README.md](docs/Python310/README.md) | custom  | Python 3.10.5 | 函数计算官方公共层 |
| Python310-Package-Collection | acs:fc:{region}:official:layers/Python310-Package-Collection/versions/1 | [README.md](docs/Python310-Package-Collection/README.md) | custom  | [requirements.txt](docs/Python310-Package-Collection/requirements.txt) | 函数计算官方公共层，需要和层Python310一起使用|
| Python39 | acs:fc:{region}:official:layers/Python39/versions/1 | [README.md](docs/Python39/README.md) | custom  | Python 3.9.13 | 函数计算官方公共层 |
| Python39-Package-Collection | acs:fc:{region}:official:layers/Python39-Package-Collection/versions/1 | [README.md](docs/Python39-Package-Collection/README.md) | custom  | [requirements.txt](docs/Python39-Package-Collection/requirements.txt) | 函数计算官方公共层，需要和层Python39一起使用|
| Python38 | acs:fc:{region}:official:layers/Python38/versions/1 | [README.md](docs/Python38/README.md) | custom  | Python 3.8.13 | 函数计算官方公共层 |
| Python38-Package-Collection | acs:fc:{region}:official:layers/Python38-Package-Collection/versions/1 | [README.md](docs/Python38-Package-Collection/README.md) | custom  | [requirements.txt](docs/Python38-Package-Collection/requirements.txt) | 函数计算官方公共层，需要和层Python38一起使用|
| Python36 | acs:fc:{region}:official:layers/Python36/versions/1 | [README.md](docs/Python36/README.md) | custom  | Python 3.6.15 | 函数计算官方公共层 |
| Python36-Package-Collection | acs:fc:{region}:official:layers/Python36-Package-Collection/versions/1 | [README.md](docs/Python36-Package-Collection/README.md) | custom  | [requirements.txt](docs/Python36-Package-Collection/requirements.txt) | 函数计算官方公共层，需要和层Python36一起使用|
| Dotnet6 | acs:fc:{region}:official:layers/Dotnet6/versions/1 | [README.md](docs/Dotnet6/README.md) | custom  | ASP.NET Core Runtime 6.0.5 | 函数计算官方公共层 |

### 常用依赖库
| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 备注 |
|---------|------|------|--------|-----|-----|
| Python39-Pandas1x | acs:fc:{region}:official:layers/Python39-Pandas1x/versions/1 | [README.md](docs/Python39-Pandas1x/README.md) | python3.9,custom-runtime  | pandas-1.4.3 | 函数计算官方公共层 |
| Python39-SciPy1x | acs:fc:{region}:official:layers/Python39-SciPy1x/versions/1 | [README.md](docs/Python39-SciPy1x/README.md) | python3.9,custom-runtime  | scipy-1.9.0,numpy-1.23.2 | 函数计算官方公共层 |
| Python36-SciPy1x | acs:fc:{region}:official:layers/Python36-SciPy1x/versions/1 | [README.md](docs/Python36-SciPy1x/README.md) | python3.6,custom-runtime  | scipy-1.5.4,numpy-1.19.5 | 函数计算官方公共层 |

### 阿里云 SDK
| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 | 备注 |
|---------|------|------|--------|-----|-----|
| Aliyun-DataX | acs:fc:{region}:official:layers/Aliyun-DataX/versions/1 | 阿里云 DataWorks数据集成的开源版本:[README.md](docs/Aliyun-DataX/README.md) | python2.7,python3.6,python3.9,custom-runtime  | datax_v202205 | 函数计算官方公共层 |

## 参考
- [Custom-Runtime 运行时官方文档](https://help.aliyun.com/document_detail/132042.html)