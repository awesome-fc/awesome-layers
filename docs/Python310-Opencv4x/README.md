
# 【官方公共层】Python310-Opencv4x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python310-Opencv4x/versions/2` | `python3.10`,`custom.debian10`   | opencv_python-4.7.0.68 |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Python Runtime 
若选择 Python3.10 Runtime，添加该层后可直接引用

### 基于 Custom Runtime
使用该层时，需要依赖 Python3.10 运行时，可直接引用 [Python310公共层](../Python310/README.md)
- `PYTHONPATH`环境变量需要添加 `/opt/python` 目录
- `PATH` 环境变量需要添加 `/opt/python3.10/bin` 目录，注意需要加到`PATH`的最前面

示例如下：
```shell
PYTHONPATH=/opt/python
PATH=/opt/python3.10/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## License
[Apache License 2.0](https://github.com/opencv/opencv/blob/4.x/LICENSE)

## 参考信息
维护者：阿里云-函数计算