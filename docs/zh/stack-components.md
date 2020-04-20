---
sidebarDepth: 3
---

# 参数

Kafka 预装包包含 Kafka 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

下来我们对路径信息进行更为准确的说明：

### Kafka

Kafka 安装目录：*/opt/kafka*  
Kafka 日志目录：*/opt/kafka/logs*  
Kafka bin目录：*/opt/kafka/bin*  
Kafka 配置目录：*/opt/kafka/config*  

### Java

Java 虚拟机目录： */usr/bin/java*  

### Zookeeper

Zookeeper 配置文件路径：/opt/zookeeper/conf/  
Zookeeper 日志文件：/opt/zookeeper/tmp/zookeeper.out  

## 端口号

在云服务器中，通过 **[安全组设置](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** 来控制（开启或关闭）端口是否可以被外部访问。 

通过命令`netstat -tunlp`查看相关端口，下面列出本应用可能要用到的端口：

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| TCP | 9092 | Kafka | 可选 |
| TCP | 2181 | Zookeeper | 可选 |

## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

```shell
# Linux Version
lsb_release -a

# Java  Version
java -version

# Kafka version
ls /opt/kafka/libs | grep kafka_
```