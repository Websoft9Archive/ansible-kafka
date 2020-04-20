# Start or Stop the Services

These commands you must know when you using the Kafka of Websoft9

## Kafka

```shell
sudo systemctl start kafka
sudo systemctl stop kafka
sudo systemctl restart kafka
sudo systemctl status kafka

# you can use this debug mode if Kafka service can't run
bash /opt/kafka/bin/kafka-server-start.sh
```

## Zookeeper

```shell
sudo systemctl start zookeeper
sudo systemctl stop zookeeper
sudo systemctl restart zookeeper
sudo systemctl status zookeeper

# you can use this debug mode if Kafka service can't run
bash /opt/kafka/bin/zookeeper-server-start.sh
```