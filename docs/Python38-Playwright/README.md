
# 【官方公共层】Python38-Playwright

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Python38-Playwright/versions/1` | `custom.debian10`   | playwright==1.31.1 |

> 注意：官方公共层 `Python38-Playwright` 仅支持 `custom.debian10` 运行时下的 `Python3.8`版本。
> 不支持`cusotom`运行时，也不支持`custom.debian10`运行时下的其他Python版本。

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Custom Runtime (Debian10)
使用该层时，需要依赖 Python3.8 运行时，可直接引用 [Python38公共层](../Python38/README.md)
- `PYTHONPATH`环境变量需要添加 `/opt/python` 目录
- `PATH` 环境变量需要添加 `/opt/python3.8/bin` 目录，注意需要加到`PATH`的最前面
- `LD_LIBRARY_PATH` 环境变量需要添加 `/opt/lib` 目录

示例如下：
```shell
PATH=/opt/python3.8/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
PYTHONPATH=/opt/python
LD_LIBRARY_PATH=/opt/lib
```

## License
[Apache-2.0](https://github.com/microsoft/playwright/blob/main/LICENSE)

## 参考信息
维护者：阿里云-函数计算