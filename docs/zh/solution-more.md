# 更多...

下面每一个方案，都经过实践证明行之有效，希望能够对你有帮助

## 日志清理

### 启用默认日志清理策略

Kafka 默认设置保留 7 天日志，但默认并为启用日志清理策略。运行如下命令后启用：

```
# 打开日志删除策略
sed -i '/log.retention.hours=168/i\log.cleanup.policy=delete' /opt/kafka/config/server.properties

# 重启Kafka
systemctl restart kafka
```

### 自定义日志清理策略

用户可以自定义日志清理策略，具体步骤如下：

1. 修改 */opt/kafka/config/server.propertie*  文件中相关的参数
    ```
    log.cleanup.policy=delete #添加 启用删除策略配置段
    log.retention.hours=168    #默认7天
    log.retention.check.interval.ms=300000 #默认每5分钟检查一次
    log.segment.bytes=1073741824 #默认每个segment的大小为1GB
    ```

2. 修改后重启 Kafka 服务
    ```
    systemctl restart kafka
    ```
