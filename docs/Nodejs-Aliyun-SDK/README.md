# 【官方公共层】Nodejs-Aliyun-SDK

| ARN                                                              | 兼容运行时                    | 版本                |
|------------------------------------------------------------------|--------------------------|-------------------|
| `acs:fc:{region}:official:layers/Nodejs-Aliyun-SDK/versions/2` | `nodejs16`, `nodejs14`, `nodejs12`, `custom` |  |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Nodejs Runtime
若选择 Nodejs Runtime，添加该层后可直接使用。

> 如果环境变量中修改了 `NODE_PATH`，需要添加以下路径
> - `NODE_PATH=/opt/nodejs/node_modules`

### 基于 Custom Runtime

添加以下环境变量
- `NODE_PATH=/opt/nodejs/node_modules`

## License
- cloudevents: [Apache-2](https://github.com/cloudevents/sdk-javascript/blob/main/LICENSE)
- ali-oss: [MIT](https://github.com/ali-sdk/ali-oss/blob/master/LICENSE)
- aliyun/fc2: [MIT](https://github.com/aliyun/fc-nodejs-sdk/blob/master/LICENSE)

## 参考信息
维护者：阿里云-函数计算