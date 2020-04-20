# Start or Stop the Services

These commands you must know when you using the Kafka of Websoft9

## Kafka

```shell
sudo systemctl start rabbitmq-server
sudo systemctl stop rabbitmq-server
sudo systemctl restart rabbitmq-server
sudo systemctl status rabbitmq-server

# you can use this debug mode if Kafka service can't run
rabbitmq-server console
```