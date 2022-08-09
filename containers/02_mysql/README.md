# MySQL

<https://www.mysql.com/>

## docker 部署

<https://hub.docker.com/_/mysql>

```shell
$ docker pull mysql:8.0.29

$ docker volume create mysql-data

# docker run -it --rm mysql:8.0.29 --verbose --help
$ docker run -d --name chaos-mysql \
	-p 3306:3306 \
	-e MYSQL_ROOT_PASSWORD=mysql@chaos \
	-v mysql-data:/var/lib/mysql \
	mysql:8.0.29 --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci

# root/mysql@chaos
```

## Schema

## 客户端

- <https://www.mysql.com/products/workbench/>
- navicat