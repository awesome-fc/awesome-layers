
# 【官方公共层】Python36-SciPy1x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python36-SciPy1x/versions/1` | custom-runtime   | scipy-1.5.4,numpy-1.19.5 |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Python Runtime 
若选择 Python3.6 Runtime，添加该层后可直接引用

### 基于 Custom Runtime
使用该层时，需要依赖 Python3.6 运行时，可直接引用 [Python36公共层](../Python36/README.md)
- `PYTHONPATH`环境变量需要添加 `/opt/python` 目录
- `PATH` 环境变量需要添加 `/opt/python3.6/bin` 目录，注意需要加到`PATH`的最前面

示例如下：
```shell
PYTHONPATH=/opt/python
PATH=/opt/python3.6/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## License
[BSD-3](https://github.com/scipy/scipy/blob/main/LICENSE.txt)

## 参考信息
维护者：阿里云-函数计算