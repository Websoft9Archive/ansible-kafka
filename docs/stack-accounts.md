# Username and Password

These accounts are required for Kafka image installation and configuration

Use the **SSH** to connect your Server and run the command `sudo cat /credentials/password.txt` to get the username and password of this deployment solution.

![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

Here are the required username and password for RabbitMQ installation and configuration.

## Kafka

No credentials

## CMAK

* CMAK administrator username: `admin`
* CMAK administrator password: Get it form the file of your server */credentials/password.txt*

## Linux

* Host Name: Server's Internet IP or Public IP of your Instance
* Connect by: Online SSH on Cloud Console or SFTP/SSH tools on your local computer
* Password: It was set by yourself when created instance.
* Username: Different Cloud Platform has differences.
   |  Cloud Platform   |  Administrator Username   | Other |
   | --- | --- | --- |
   |  Azure   |  It was set by yourself when created instance.   | [How to enable root access?](https://support.websoft9.com/docs/azure/server-login.html#sample2-enable-the-root-username) |
   |  AWS CentOS   |  centos   | [How to enable root access?](https://support.websoft9.com/docs/aws/server-login.html#sample2-enable-the-root-username) |
   |  AWS AmaonLinux   |  ec2-user   | [How to enable root access?](https://support.websoft9.com/docs/aws/server-login.html#sample2-enable-the-root-username) |
   |  AWS Ubuntu   |  ubuntu   | [How to enable root access?](https://support.websoft9.com/docs/aws/server-login.html#sample2-enable-the-root-username) |
   |  Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud |  root   |

   > If you forgot the password of Linux, reset it on Cloud Console.
