# Initial Installation

If you have completed the Kafka deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:9092,2181 is allowed

## Kafka Installation check

Use you **SSH** to login Server, run the following commands

```
systemctl status kafka
systemctl status zookeeper
bash /opt/kafka/bin/kafka-configs.sh
```

> Refer to the Kafka official docs for your quick start: [Kafka Quickstart](https://kafka.apache.org/quickstart)

## Q&A

#### Run the command "kafka-topics.sh", java not found?

You should add a variable $JAVA_HOME=/usr/bin/java

#### Is Java included in this deployment solution?

Yes