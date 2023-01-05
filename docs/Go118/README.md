
# 【官方公共层】Go118

| ARN                                                |  兼容运行时  | 版本        |
|----------------------------------------------------|------|-----------|
| `acs:fc:{region}:official:layers/Go118/versions/1` | custom-runtime   | go 1.18.8 |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

使用`Go118`层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。
- `PATH` 环境变量需要添加 `/opt/go1.18.8/bin` 目录，注意需要加到`PATH`的最前面

示例如下：
```shell
PATH=/opt/go1.18.8/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## 应用示例
待补充

## License
[BSD-3](https://github.com/golang/go/blob/master/LICENSE)

## 参考信息
维护者：阿里云-函数计算