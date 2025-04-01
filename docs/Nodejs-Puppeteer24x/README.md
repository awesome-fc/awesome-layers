# 【官方公共层】Nodejs-Puppeteer24x

| ARN                                                              | 兼容运行时                    | 版本                |
|------------------------------------------------------------------|--------------------------|-------------------|
| `acs:fc:{region}:official:layers/Nodejs-Puppeteer24x/versions/1` | `custom.debian10` | puppeteer-v24.4.0 |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

### 基于 Custom Runtime (Debian12)

添加以下两个环境变量

```bash
FONTCONFIG_FILE=/opt/etc/fonts.conf
PUPPETEER_CACHE_DIR=/opt/cache/puppeteer
```

## License

[Apache-2](https://github.com/puppeteer/puppeteer/blob/main/LICENSE)

## 参考信息

维护者：阿里云-函数计算