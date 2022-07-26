# redis

<https://redis.io/>

## docker 部署

<https://hub.docker.com/_/redis>

```shell
$ docker pull redis:5.0.14

$ docker volume create redis-data

$ docker run -d --name chaos-redis \
	-p 6379:6379 \
    -v redis-data:/data \
	redis:5.0.14 redis-server --port 6379
```

## 客户端

- <https://redis.com/redis-enterprise/redis-insight/>