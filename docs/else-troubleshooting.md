# Troubleshooting

We collect the most common troubleshooting of using Kafka for your reference:

#### How can I use the logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### Kafka service can't start?

1. Use the debug mode of `bash /opt/kafka/bin/kafka-server-start.sh` and you can see the errors
2. Search the keywords **Failed** or **error** from logs: */data/logs*

#### Run the command "kafka-topics.sh", java not found?

You should add a variable $JAVA_HOME=/usr/bin/java