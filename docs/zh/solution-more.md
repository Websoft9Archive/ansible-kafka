# 更多...

下面每一个方案，都经过实践证明行之有效，希望能够对你有帮助

## 启用默认日志清理策略

默认设置保留7天日志,但是策略未启用<br />输入一下命令:

```
# 打开日志删除策略
sed -i '/log.retention.hours=168/i\log.cleanup.policy=delete' /opt/kafka/config/server.properties

# 重启Kafka
systemctl restart kafka
```
## 自定义日志清理策略

修改 /opt/kafka/config/server.properties 一下参数的值

```
log.cleanup.policy=delete #添加 启用删除策略配置段
log.retention.hours=168    #默认7天
log.retention.check.interval.ms=300000 #默认每5分钟检查一次
log.segment.bytes=1073741824 #默认每个segment的大小为1GB

# 修改后重启Kafka
systemctl restart kafka
```
