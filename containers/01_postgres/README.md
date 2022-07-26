# PostgreSQL

<https://www.postgresql.org/>

## docker 部署

<https://hub.docker.com/_/postgres>

```shell
$ docker pull postgres:13.7

$ docker volume create postgres-data

$ docker run -d --name chaos-postgres \
	-p 5432:5432 \
	-e POSTGRES_PASSWORD=postgres@chaos \
	-e ALLOW_IP_RANGE=0.0.0.0/0 \
	-e PGDATA=/var/lib/postgresql/data/pgdata \
	-v postgres-data:/var/lib/postgresql/data \
	postgres:13.7
```

## 客户端

- <https://www.pgadmin.org/>  master-password : 1qaz2wsx