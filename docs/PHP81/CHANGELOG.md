
## 2022-09-15 Version 4
ARN: `acs:fc:{region}:official:layers/PHP81/versions/4`
- enable php-fpm (/opt/php8.1/sbin/php-fpm)

## 2022-09-15 Version 3
ARN: `acs:fc:{region}:official:layers/PHP81/versions/3`
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
ARN: `acs:fc:{region}:official:layers/PHP81/versions/2`