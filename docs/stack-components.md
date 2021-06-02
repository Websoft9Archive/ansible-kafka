# Parameters

The Kafka deployment package contains a sequence software (referred to as "components") required for Kafka to run. The important information such as the component name, installation directory path, configuration file path, port, version, etc. are listed below.

## Path

We have prepared the component path detail for your reference:

### Kafka

Kafka installation directory:*/opt/kafka*  
Kafka installation log directory:*/opt/kafka/logs*  
Kafka bin directory: */opt/kafka/bin*  
Kafka configuration directory: */opt/kafka/config*  

### Java

JVM directory: */usr/bin/java*  

### CMAK

[CMAK](https://github.com/yahoo/CMAK) is cluster Manager for Apache Kafka, is installed based on Docker

CMAK directory: */data/apps/cmak*  

### Zookeeper

Zookeeper configuration directory: /opt/zookeeper/conf/  
Zookeeper log file: /opt/zookeeper/tmp/zookeeper.out  

## Ports

You can control(open or shut down) ports by **[Security Group Setting](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** of your Cloud Server whether the port can be accessed from Internet.

You can run the cmd `netstat -tunlp` to list all used ports, and we list the following most useful ports for you:

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| TCP | 9092 | Kafka | Optional |
| TCP | 2181 | Zookeeper | Optional |
| TCP | 9091 | CMAK | Optional |


## Version

You can see the version from product page of Marketplace. However, after being deployed to your server, the components will be automatically updated, resulting in a certain change in the version number. Therefore, the exact version number should be viewed by running the command on the server:

```shell
# Linux Version
lsb_release -a

# Java  Version
java -version

# Kafka version
ls /opt/kafka/libs | grep kafka_
```