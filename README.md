# 阿里云-函数计算-公共层

该项目提供了一些精选的函数计算公共层。
层可以为您提供自定义的公共依赖库、运行时环境及函数扩展等发布与部署能力。您可以直接使用本文列举的公共层，以减少部署、更新时的代码包体积，也可以快速的开发和测试您的代码。

详细信息可参考官方文档
- [构建层](https://help.aliyun.com/document_detail/193057.html)
- [使用层](https://help.aliyun.com/document_detail/193058.html)

## 公共层
公共层主要分为以下几类:
- 运行时
- 运行时依赖库集合
- 阿里云 SDK

### 运行时
| 层名称  | ARN  | 说明 | 兼容运行时  | 版本 |
|---------|------|------|--------|-----|
| Python310 | acs:fc:{region}:official:layers/Python310/versions/1 | [README.md](docs/Python310/README.md) | custom   | Python 3.10.5 |


## 参考
- [Custom-Runtime 运行时官方文档](https://help.aliyun.com/document_detail/132042.html)