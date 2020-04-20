# 故障处理

此处收集使用 Kafka 过程中最常见的故障，供您参考

> 大部分故障与云平台密切相关，如果你可以确认故障的原因是云平台造成的，请参考[云平台文档](https://support.websoft9.com/docs/faq/zh/tech-instance.html)

#### 如何查看错误日志？

日志文件路径为：`/data/logs`。检索关键词 **Failed** 或者 **error** 查看错误

#### Kafka服务无法启动？

1. 以调试模式运行`bash /opt/kafka/bin/kafka-server-start.sh`，便可以查看启动状态和错误
2. 打开日志文件：*/data/logs*，检索 **failed** 关键词，分析错误原因

#### 运行 *kafka-run-class.sh* 显示 **java: not found...**的错误？

这是Java环境变量缺失导致的问题，请设置环境变量：$JAVA_HOME=/usr/bin/java
