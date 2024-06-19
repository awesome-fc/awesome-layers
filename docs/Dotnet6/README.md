
# 【官方公共层】Dotnet6

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Dotnet6/versions/3` | `custom`,`custom.debian10`   | ASP.NET Core Runtime 6.0.5 |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

使用`Dotnet6`层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。

- `PATH` 环境变量需要添加 `/opt/dotnet6` 目录，注意需要加到`PATH`的最前面

示例如下：

```shell
PATH=/opt/dotnet6:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
```

## 应用示例

详见：<http://www.devsapp.cn/details.html?name=start-fc-http-aspdotnetcore6>

## License

[.NET is Free](https://dotnet.microsoft.com/en-us/platform/free)

## 参考信息

维护者：阿里云-函数计算
