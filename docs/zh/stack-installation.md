# 初始化安装

在云服务器上部署 Kafka 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:9092,2181** 端口是否开启

## Kafka 检查

使用SSH登录到服务器后，运行如下几个命令，检查Kafka是否正确安装

```
systemctl status kafka
systemctl status zookeeper
bash /opt/kafka/bin/kafka-configs.sh
```

> 需要了解更多 Kafka 的使用，请参考官方文档：[Kafka Quickstart](https://kafka.apache.org/quickstart)

## 常见问题

#### 运行 *kafka-run-class.sh* 显示 **java: not found...**的错误？

这是Java环境变量缺失导致的问题，请设置环境变量：$JAVA_HOME=/usr/bin/java

#### 本部署环境中是否已经包含Java？

是的