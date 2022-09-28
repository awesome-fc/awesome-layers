
# 【官方公共层】Aliyun-DataX

| ARN  |  兼容运行时  | 版本 |
|------|------|--------|
| `acs:fc:{region}:official:layers/Aliyun-DataX/versions/1` | python2.7,python3.6,python3.9,custom-runtime   | datax_v202205  |

阿里云 DataWorks 数据集成的开源版本。
源代码：[DataX](https://github.com/alibaba/DataX)

## 快速开始
可以通过控制台或者 Serverless Devs 工具引用该层。

该层的依赖包括：
- Linux
- JDK(1.8以上，推荐1.8)
- Python(2或3都可以)
- Apache Maven 3.x (Compile DataX)
参考文档：https://github.com/alibaba/DataX/blob/master/userGuid.md

函数计算的Python运行时环境中默认包含了JDK，因此可以直接使用，但是Custom-Runtime没有JDK，需要添加JDK依赖层。

### 基于 Python Runtime 
基于 Python Runtime使用该层时，需要配置相应的环境变量。
- `PATH` 环境变量需要添加 `/var/fc/lang/java8/bin` 目录
- `JAVA_HOME` 环境变量需要设置为 `/var/fc/lang/java8` 

示例如下：
```shell
JAVA_HOME=/var/fc/lang/java8
PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/bin:/var/fc/lang/java8/bin
```

## 应用示例
详见：[ServerlessDataXTransfer](http://www.devsapp.cn/details.html?name=ServerlessDataXTransfer)

## License
[Apache-2](https://github.com/alibaba/DataX/blob/master/license.txt)

## 参考信息
维护者：阿里云-函数计算