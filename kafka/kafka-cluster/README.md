## 前提准备

1. 修改`.env`中的变量为你的实际数据。

## 启动服务

```shell
docker-compose up -d
```

## 验证服务

进入`kafka01`容器中，查询三个`broker`在线状态：
```shell
# 宿主机中执行
[lbs@test kafka-cluster]$ docker-compose exec kafka01 bash
# 进入容器后执行
I have no name!@dc4a4d00df07:/$ zookeeper-shell.sh zookeeper01:2181 ls /brokers/ids
Connecting to zookeeper:2181

WATCHER::

WatchedEvent state:SyncConnected type:None path:null
[1, 2, 3]
```
