
# 【官方公共层】Nodejs-Puppeteer10x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Nodejs-Puppeteer10x/versions/1` | custom-runtime   | puppeteer-v10.2.0 |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Nodejs Runtime 
若选择 Nodejs Runtime，添加该层后需要配置以下环境变量
- `NODE_PATH=/opt/node_modules:/opt/nodejs/node_modules`
- `LD_LIBRARY_PATH=/opt/lib/x86_64-linux-gnu:/opt/lib`

### 基于 Custom Runtime
待补充

## License
[Apache-2](https://github.com/puppeteer/puppeteer/blob/main/LICENSE)

## 参考信息
维护者：阿里云-函数计算