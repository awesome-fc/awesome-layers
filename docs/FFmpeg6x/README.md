
# 【官方公共层】FFmpeg6x

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/FFmpeg6x/versions/1` | `custom`,`custom.debian10`,`python3.10`,`python3.9`,`nodejs16`,`nodejs14`,`java11`,`java8`   |  6.0  |

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

`ffmpeg`等可执行文件zip包的`bin`目录下下，在函数计算中会解压到 `/opt` 目录下，在函数计算运行环境内，`sqlite`的完整路径是`/opt/bin/ffmpeg`。

## License
https://ffmpeg.org/legal.html

## 参考信息
维护者：阿里云-函数计算