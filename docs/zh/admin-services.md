# 服务启停

使用由Websoft9提供的 Kafka 部署方案，可能需要用到的服务如下：

### Kafka

```shell
sudo systemctl start kafka
sudo systemctl stop kafka
sudo systemctl restart kafka
sudo systemctl status kafka

# you can use this debug mode if Kafka service can't run
bash /opt/kafka/bin/kafka-server-start.sh
```

### Zookeeper

```shell
sudo systemctl start zookeeper
sudo systemctl stop zookeeper
sudo systemctl restart zookeeper
sudo systemctl status zookeeper

# you can use this debug mode if Kafka service can't run
bash /opt/kafka/bin/zookeeper-server-start.sh
```

### Docker
```shell
sudo systemctl start docker
sudo systemctl stop docker
sudo systemctl restart docker
sudo systemctl status docker
```

### CMAK
```shell
sudo docker inspect cmak
sudo docker start cmak
sudo docker restart cmak
sudo docker stop cmak
sudo docker rm cmak
```
