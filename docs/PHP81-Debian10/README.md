
# 【官方公共层】PHP81-Debian10

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/PHP81-Debian10/versions/1` | `custom.debian10`   | PHP 8.1.28 |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

使用`PHP81-Debian10`层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。

- `PATH` 环境变量需要添加 `/opt/php8.1/bin` 和 `/opt/php8.1/sbin` 目录，注意需要加到`PATH`的最前面
- `LD_LIBRARY_PATH` 环境变量需要添加 `/opt/php8.1/lib`目录

示例如下：

```shell
PATH=/opt/php8.1/bin:/opt/php8.1/sbin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
LD_LIBRARY_PATH=/code:/code/lib:/usr/local/lib:/opt/lib:/opt/php8.1/lib
```

## 应用示例

待补充

## License

[PHP License v3.01](https://www.php.net/license/3_01.txt)

## 参考信息

维护者：阿里云-函数计算
