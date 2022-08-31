
# 【官方公共层】Java11

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Java11/versions/1` | custom-runtime   | openjdk 11.0.13 |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

使用`Java11`层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。
- `PATH` 环境变量需要添加 `/opt/Java11/bin` 目录，注意需要加到`PATH`的最前面

示例如下：
```shell
PATH=/opt/Java11/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## 应用示例
待补充

## License
[GPLv2](https://openjdk.org/legal/gplv2+ce.html)

## 参考信息
维护者：阿里云-函数计算