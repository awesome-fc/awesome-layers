
# 【官方公共层】Python39-PyTorch1x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python39-PyTorch1x/versions/2` | `python3.9`, `custom`, `custom.debian10`  | torch==1.12.1+cpu,torchaudio==0.12.1+cpu,torchvision==0.13.1+cpu |
| `acs:fc:{region}:official:layers/Python39-PyTorch1x/versions/1` | `python3.9`, `custom`  | torch==1.12.1+cpu,torchaudio==0.12.1+cpu,torchvision==0.13.1+cpu |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Python Runtime 
若选择 Python3.9 Runtime，添加该层后可直接引用

### 基于 Custom Runtime
使用该层时，需要依赖 Python3.9 运行时，可直接引用 [Python39公共层](../Python39/README.md)
- `PYTHONPATH`环境变量需要添加 `/opt/python` 目录
- `PATH` 环境变量需要添加 `/opt/python3.9/bin` 目录，注意需要加到`PATH`的最前面

示例如下：
```shell
PYTHONPATH=/opt/python
PATH=/opt/python3.9/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## License
[BSD](https://github.com/pytorch/pytorch/blob/master/LICENSE)

## 参考信息
维护者：阿里云-函数计算