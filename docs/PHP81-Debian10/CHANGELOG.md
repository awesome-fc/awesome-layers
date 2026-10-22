# 2026-10-22 Version 2

ARN: `acs:fc:{region}:official:layers/PHP81-Debian10/versions/2`

- PHP 版本号保持 8.1.28，回补 CVE-2026-109618、CVE-2026-109619；兼容运行时和安装路径保持 `custom.debian10`、`/opt/php8.1`。
- 内存耗尽或内存分配大小溢出时立即退出，不再执行通过 `register_shutdown_function()` 注册的回调和对象析构函数；会话上传进度功能已在源码中关闭，不能通过 `php.ini` 重新开启。
- 升级时请验证扩展、文件上传、会话功能及实际请求处理流程。详见 [安全升级指引](../PHP_SECURITY_UPGRADE.md)。


# 2024-05-06 Version 1

ARN: `acs:fc:{region}:official:layers/PHP81-Debian10/versions/1`

```ini
[PHP Modules]
bcmath
bz2
calendar
Core
ctype
curl
date
dom
exif
FFI
fileinfo
filter
ftp
gd
gettext
gmp
hash
iconv
imagick
intl
json
libxml
mbstring
mcrypt
memcached
mongodb
mysqli
mysqlnd
openssl
pcntl
pcre
PDO
pdo_mysql
pdo_sqlite
Phar
posix
protobuf
readline
redis
Reflection
session
shmop
SimpleXML
soap
sockets
SPL
sqlite3
standard
swoole
sysvmsg
sysvsem
sysvshm
tokenizer
xml
xmlreader
xmlrpc
xmlwriter
Zend OPcache
zip
zlib

[Zend Modules]
Zend OPcache
```
