
# 【官方公共层】Python39-Package-Collection

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python39-Package-Collection/versions/1` | custom-runtime   | [requirements.txt](requirements.txt) |

该层基于 Python39 层制作。

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。
有两种使用该层的方法

### 【推荐】和层 Python39 一起使用

该层需要依赖 `Python3.9` 环境，建议与层 [Python39](../Python39/README.md) 一起使用。

使用该层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。
`PATH` 环境变量需要添加 `/opt/python3.9/bin` 目录
> 注意需要加到`PATH`的最前面

示例如下：
```shell
PATH=/opt/python3.9/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

### 【不推荐】单独使用
如果单独使用该层，需要修改`PYTHONPATH`环境变量，添加路径 `/opt/python3.9/lib/python3.9/site-packages`

示例如下：
```shell
PYTHONPATH=/opt/python3.9/lib/python3.9/site-packages:/opt/python
```

## License
[docker-library/python: License](https://github.com/docker-library/python/blob/7b9d62e229bda6312b9f91b37ab83e33b4e34542/LICENSE)

## 参考信息
维护者：阿里云-函数计算