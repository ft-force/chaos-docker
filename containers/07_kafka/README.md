# Kafka

<https://kafka.apache.org/>

## docker 部署

- <https://hub.docker.com/r/wurstmeister/kafka>

```shell
$ docker pull wurstmeister/kafka:2.13-2.8.1

$ docker volume create kafka-data

$ docker run -d --name chaos-kafka \
    -p 9092:9092 \
    -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181 \
    -e KAFKA_ADVERTISED_PORT=9092 \
    -e KAFKA_BROKER_ID=1 \
    -e KAFKA_LISTENERS=PLAINTEXT://:9092 \
    -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://:9092 \
    -v kafka-data:/KAFKA \
    --link chaos-zookeeper:zookeeper \
	wurstmeister/kafka:2.13-2.8.1
```
