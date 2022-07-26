# MongoDB

<https://www.mongodb.com/>

## docker 部署

<https://hub.docker.com/_/mongo>

```shell
$ docker pull mongo:5.0.9

$ docker volume create mongo-data
$ docker volume create mongo-config-data


# docker run -it --rm mongo:5.0.9 --help
$ docker run -d --name chaos-mongo \
	-p 27017:27017 \
    -e MONGO_INITDB_ROOT_USERNAME=admin \
    -e MONGO_INITDB_ROOT_PASSWORD=mongo@chaos \
    -v mongo-data:/data/db \
    -v mongo-config-data:/data/configdb \
	mongo:5.0.9 --auth
```

## 客户端

- navicat
