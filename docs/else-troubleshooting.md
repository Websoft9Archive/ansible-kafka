# Troubleshooting

We collect the most common troubleshooting of using Kafka for your reference:

> Instance troubleshooting is closely related to the Instance provider that is Cloud Platform, refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html)

#### How can I use the logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### Kafka service can't start?

1. Use the debug mode of `bash /opt/kafka/bin/kafka-server-start.sh` and you can see the errors
2. Search the keywords **Failed** or **error** from logs: */data/logs*

#### Run the command "kafka-topics.sh", java not found?

You should add a variable $JAVA_HOME=/usr/bin/java
