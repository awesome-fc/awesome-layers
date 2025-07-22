# 【官方公共层】Nodejs-Puppeteer17x

| ARN                                                              | 兼容运行时                    | 版本                |
|------------------------------------------------------------------|--------------------------|-------------------|
| `acs:fc:{region}:official:layers/Nodejs-Puppeteer17x/versions/3` | `nodejs16`, `nodejs14`, `custom.debian10` | puppeteer-v17.1.0 |
| `acs:fc:{region}:official:layers/Nodejs-Puppeteer17x/versions/2` | `nodejs16`, `nodejs14`, `custom` | puppeteer-v17.1.0 |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

> 注意：内存规格建议大于 1024 MB。

### 基于 Nodejs Runtime
若选择 Nodejs Runtime，添加该层后可直接使用。

> 如果环境变量中修改了 `NODE_PATH` 或 `LD_LIBRARY_PATH`，需要添加以下路径
> - `NODE_PATH=/opt/node_modules:/opt/nodejs/node_modules`
> - `LD_LIBRARY_PATH=/opt/lib`

### 基于 Custom Runtime

添加以下两个环境变量
- `NODE_PATH=/opt/node_modules:/opt/nodejs/node_modules`
- `LD_LIBRARY_PATH=/opt/lib`

## License
[Apache-2](https://github.com/puppeteer/puppeteer/blob/main/LICENSE)

## 参考信息
维护者：阿里云-函数计算