# 【官方公共层】PHP85-Debian12

PHP 8.5.12 / Debian 12（Bookworm），仅适用于 `custom.debian12` 的 x86_64（amd64）函数，安装路径为 `/opt/php8.5`。

| 目标 ARN（待正式发布） | 兼容运行时 | PHP 版本 |
| --- | --- | --- |
| `acs:fc:{region}:official:layers/PHP85-Debian12/versions/1` | `custom.debian12` | PHP 8.5.12 |

将 `{region}` 替换为函数所在地域。公共层版本 `1` 与 PHP 版本 `8.5.12` 是两个不同的版本号。

## 快速开始

正式发布后，可以通过控制台或 Serverless Devs 为 `custom.debian12` 函数配置该层。函数启动命令设置为 `/bin/bash /code/bootstrap`，监听端口设置为 `9000`。

在函数代码中创建 `bootstrap`，设置环境变量并启动应用：

```sh
#!/bin/bash
export PATH=/opt/php8.5/bin:/opt/php8.5/sbin:$PATH
export LD_LIBRARY_PATH=/opt/php8.5/lib${LD_LIBRARY_PATH:+:$LD_LIBRARY_PATH}
export SSL_CERT_FILE=/opt/php8.5/ssl/cert.pem
export MAGICK_CONFIGURE_PATH=/opt/php8.5/etc/ImageMagick-6
export MAGICK_CODER_MODULE_PATH=/opt/php8.5/lib/ImageMagick/modules-Q16/coders
export MAGICK_FILTER_MODULE_PATH=/opt/php8.5/lib/ImageMagick/modules-Q16/filters
exec /opt/php8.5/bin/php /code/server.php
```

`server.php` 由业务提供，需要监听 `0.0.0.0`，端口与函数配置一致。例如使用层内的 Swoole 启动一个简单 HTTP 服务：

```php
<?php
$server = new Swoole\Http\Server('0.0.0.0', 9000, SWOOLE_BASE);
$server->on('request', function ($request, $response): void {
    $response->header('Content-Type', 'text/plain; charset=utf-8');
    $response->end("Hello from PHP 8.5\n");
});
$server->start();
```

CLI、CGI 和 FPM 入口分别为 `/opt/php8.5/bin/php`、`/opt/php8.5/bin/php-cgi` 和 `/opt/php8.5/sbin/php-fpm`。FPM 使用 FastCGI，需要应用提供 HTTP 网关，不能直接作为 FC HTTP 监听服务。

## 扩展

内置 SQLite、MySQL、PostgreSQL、curl/OpenSSL、intl、mbstring、GD、zip、sodium、FFI、SOAP 等常用扩展。PHP 配置文件位于 `/opt/php8.5/etc/php/php.ini`，附加配置位于 `/opt/php8.5/etc/php/conf.d/`。

| 扩展 | 版本 | 默认加载 |
| --- | --- | --- |
| Redis | 6.3.0 | 是 |
| Imagick | 3.8.1 | 是 |
| Protobuf | 5.36.2 | 是 |
| Memcached | 3.4.0 | 是 |
| MongoDB | 2.5.5 | 是 |
| Swoole | 6.2.3 | 是 |
| Xdebug | 3.5.3 | 否 |

使用 Imagick 时保留上述 `MAGICK_*` 环境变量；层内保留 ImageMagick 默认安全策略。

## 迁移说明

- 本层使用 [PHP 8.5.12 官方安全版本](https://www.php.net/releases/8_5_12.php)，包含 CVE-2026-109618、CVE-2026-109619 修复，保留上游正常的 OOM/shutdown 和会话上传进度行为。
- 从 PHP 8.0/8.1 迁移时，需要检查 PHP 8.2–8.5 的不兼容变化、Composer 依赖、框架及原生扩展。Swoole、MongoDB、Protobuf 存在大版本变化，不能直接复制旧版 `.so` 文件。
- PHP 8.5 的 OPcache 已内置，不要沿用 `zend_extension=opcache.so`。本层不包含 XMLRPC、mcrypt 或 phpdbg；Xdebug 默认关闭。
- 本层不兼容 `custom`、`custom.debian10` 或 `custom.debian11`。已有 PHP80/PHP81 函数不会自动升级，需要同时调整运行时、层 ARN 和启动路径，并完成业务验证。
- [PHP 8.5 官方安全支持](https://www.php.net/supported-versions.php)截至 2029-12-31。

## License

[PHP License v3.01](https://www.php.net/license/3_01.txt)。各扩展保留自身许可证。

## 参考信息

维护者：阿里云-函数计算
