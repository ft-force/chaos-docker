# ZooKeeper

<https://zookeeper.apache.org/>

## docker 部署

- <https://hub.docker.com/_/zookeeper>

```shell
$ docker pull zookeeper:3.6.3

$ docker volume create zookeeper-conf-data
$ docker volume create zookeeper-data-data
$ docker volume create zookeeper-datalog-data
$ docker volume create zookeeper-logs-data

$ docker run -d --name chaos-zookeeper \
    -p 2181:2181 \
    -v zookeeper-conf-data:/conf \
    -v zookeeper-data-data:/data \
    -v zookeeper-datalog-data:/datalog \
    -v zookeeper-logs-data:/logs \
	zookeeper:3.6.3
```
