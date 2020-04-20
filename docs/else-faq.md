# FAQ

#### How can I enable the debug mode of Kafka service?

```
systemctl stop rabbitmq-server
rabbitmq-server console
```

#### Can I reset password of Kafka by command?

Yes, e.g `rabbitmqctl change_password  admin newpassword`

#### If there is no domain name, can I deploy Kafka?

Yes, visit Kafka by *http://Internet IP:8161*

#### Is it possible to modify the source path of Kafka?

No

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a sequence of software in sequence in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference, just the terminology used by different manufacturers, actually cloud servers