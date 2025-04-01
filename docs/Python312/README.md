
# 【官方公共层】Python310

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python312/versions/1` | `custom.debian12`   | Python 3.12.9 |

该层基于 Python 官方 [Dockerfile](https://github.com/docker-library/python/blob/master/3.12/bookworm/Dockerfile) 制作。

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

使用`Python3.12`层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。
- `PATH` 环境变量需要添加 `/opt/python3.12/bin` 目录，注意需要加到`PATH`的最前面

示例如下：
```shell
PATH=/opt/python3.12/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## License
[docker-library/python: License](https://github.com/docker-library/python/blob/7b9d62e229bda6312b9f91b37ab83e33b4e34542/LICENSE)

## 参考信息
维护者：阿里云-函数计算