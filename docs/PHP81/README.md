
# 【官方公共层】PHP81

> v7 包含 CVE-2026-109618、CVE-2026-109619 的安全补丁，PHP 版本号保持不变。v6 及以前的版本不建议继续使用，请升级到 v7。兼容性变化和升级步骤请参见 [PHP 公共层安全升级指引](../PHP_SECURITY_UPGRADE.md)。

| ARN | 兼容运行时 | PHP 版本 | 详情 |
| --- | --- | --- | --- |
| `acs:fc:{region}:official:layers/PHP81/versions/7` | custom-runtime | PHP 8.1.9 | 已修复 CVE-2026-109618、CVE-2026-109619，推荐使用。 |
| `acs:fc:{region}:official:layers/PHP81/versions/6` | custom-runtime | PHP 8.1.9 | 存在上述安全漏洞，不推荐使用，请升级到 v7。 |

## 快速开始

可以通过控制台或者 Serverless Devs 工具引用该层。

使用`PHP81`层时，需要配置相应的环境变量 (通过控制台创建会自动配置)。

- `PATH` 环境变量需要添加 `/opt/php8.1/bin` 和 `/opt/php8.1/sbin` 目录，注意需要加到`PATH`的最前面
- `LD_LIBRARY_PATH` 环境变量需要添加 `/opt/php8.1/lib`目录

示例如下：

```shell
PATH=/opt/php8.1/bin:/opt/php8.1/sbin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin
LD_LIBRARY_PATH=/code:/code/lib:/usr/local/lib:/opt/lib:/opt/php8.1/lib
```

### 开启XDebug

XDebug 扩展默认关闭，若要启用，需要在php.ini 文件中配置。

#### 方法1

在启动php进程前执行

```bash
echo "zend_extension=xdebug" > /opt/php8.1/etc/php/conf.d/docker-php-ext-xdebug.ini
```

#### 方法2

配置php.ini 文件，并在文件中开启 `zend_extension=xdebug`, 在启动php进程前，将配置文件拷贝到目录 `/opt/php8.1/etc/php/`.

## 应用示例

待补充

## License

[PHP License v3.01](https://www.php.net/license/3_01.txt)

## 参考信息

维护者：阿里云-函数计算
