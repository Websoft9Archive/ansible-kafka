---
sidebarDepth: 3
---

# 参数

Kafka 预装包包含 Kafka 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

虽然运行 `whereis` 命令可以查看相关安装路径，但接下来我们仍然对路径信息进行更为准确的说明。

```shell
whereis rabbitmq-server
whereis erlang

#For Centos&Redhat
rpm -ql rabbitmq-server
rpm -ql erlang

#For Ubuntu&Debian
dpkg -L rabbitmq-server
```

### Kafka

Kafka 安装目录： */data/rabbitmq*  
Kafka 日志目录： */data/logs/rabbitmq*  

### Erlang

Erlang 安装目录： */data/erlang*  

## 端口号

在云服务器中，通过 **[安全组设置](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** 来控制（开启或关闭）端口是否可以被外部访问。 

通过命令`netstat -tunlp`查看相关端口，下面列出本应用可能要用到的端口：

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| HTTP | 15672 | 通过 HTTP 访问 Kafka 控制台 | 可选 |
| TCP | 5672 | epmd | 可选 |
| TCP | 55672 | Erlang distribution | 可选 |

## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

```shell
# Linux Version
lsb_release -a

# erlang  Version
yum info erlang
apt show erlang

# Kafka version
rabbitmqctl status | grep Kafka*
```