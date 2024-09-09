
# 【官方公共层】Python312-Aliyun-SDK

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python312-Aliyun-SDK/versions/1` | `python3.12`, `custom.debian11`   | [requirements.txt](./requirements.txt) |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Python Runtime

若选择 Python3.12 Runtime，添加该层后可直接引用

### 基于 Custom Runtime (debian11)

使用该层时，需要添加以下环境变量

- `PYTHONPATH`环境变量需要添加 `/opt/python` 目录
- `PATH` 环境变量需要添加 `/var/fc/lang/python3.12/bin` 目录，注意需要加到`PATH`的最前面

示例如下：

```shell
PYTHONPATH=/opt/python
PATH=/var/fc/lang/python3.12/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## License

无

## 参考信息

维护者：阿里云-函数计算
