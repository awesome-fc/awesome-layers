
# 【官方公共层】Python3x-PyMongo4x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python3x-PyMongo4x/versions/1` | `python3.10`, `custom.debian10`   | PyMongo==4.6.1 |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Python Runtime

若选择 Python3.10 Runtime，添加该层后可直接引用

### 基于 Custom Runtime (debian10)

使用该层时，需要添加以下环境变量

- `PYTHONPATH`环境变量需要添加 `/opt/python` 目录
- `PATH` 环境变量需要添加 `/var/fc/lang/python3.10/bin` 目录，注意需要加到`PATH`的最前面

示例如下：

```shell
PYTHONPATH=/opt/python
PATH=/var/fc/lang/python3.10/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## License

[BSD-3](https://pandas.pydata.org/docs/getting_started/overview.html#license)

## 参考信息

维护者：阿里云-函数计算
