# Troubleshooting

We collect the most common troubleshooting of using Kafka for your reference:

#### How can I use the logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### Kafka service can't start?

1. Use the debug mode of `rabbitmq-server console` and you can see the errors
   ```
   rabbitmq-server console
   ```
2. Search the keywords **Failed** or **error** from logs: */data/logs/rabbitmq-server*

#### Error in Chrome when modify password?

This error is not attribute to Kafka server, once you have upgraded you local Chrome, it solved

![chrome error of Kafka](https://libs.websoft9.com/Websoft9/DocsPicture/zh/rabbitmq/rabbitmq-chromeerror-websoft9.png)