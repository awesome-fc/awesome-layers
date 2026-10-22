# 2026-10-22 Version 8

ARN: `acs:fc:{region}:official:layers/PHP80/versions/8`

- PHP 版本号保持 8.0.22，回补 CVE-2026-109618、CVE-2026-109619 的安全补丁；兼容运行时和安装路径保持 `custom`、`/opt/php8.0`。
- 内存耗尽或内存分配大小溢出时立即退出，不再执行通过 `register_shutdown_function()` 注册的回调和对象析构函数；会话上传进度功能已在源码中关闭，不能通过 `php.ini` 重新开启。
- 升级时请验证扩展、文件上传、会话功能及实际请求处理流程。详见 [安全升级指引](../PHP_SECURITY_UPGRADE.md)。

## 2024-01-17 Version 7

ARN: `acs:fc:{region}:official:layers/PHP80/versions/6`

- disable Xdebug
- update openswoole to swoole

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
json
libxml
mbstring
memcached
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

## 2023-01-05 Version 5

ARN: `acs:fc:{region}:official:layers/PHP80/versions/5`

- enable ffi
- enable gd jpeg
  
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
json
libxml
mbstring
memcached
mysqli
mysqlnd
openssl
openswoole
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
sysvmsg
sysvsem
sysvshm
tokenizer
xdebug
xml
xmlreader
xmlrpc
xmlwriter
Zend OPcache
zip
zlib

[Zend Modules]
Xdebug
Zend OPcache
```

## 2022-09-15 Version 4

ARN: `acs:fc:{region}:official:layers/PHP80/versions/4`

- enable php-fpm (/opt/php8.0/sbin/php-fpm)

## 2022-09-15 Version 3

ARN: `acs:fc:{region}:official:layers/PHP80/versions/3`

- add some extensions

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
fileinfo
filter
ftp
gd
gettext
gmp
hash
iconv
imagick
json
libxml
mbstring
memcached
mysqli
mysqlnd
openssl
openswoole
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
sysvmsg
sysvsem
sysvshm
tokenizer
xdebug
xml
xmlreader
xmlrpc
xmlwriter
Zend OPcache
zip
zlib

[Zend Modules]
Xdebug
Zend OPcache
```

## 2022-09-01 Version 2

ARN: `acs:fc:{region}:official:layers/PHP80/versions/2`
