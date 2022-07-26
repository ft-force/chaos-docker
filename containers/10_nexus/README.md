# nexus

## docker 部署

- <https://hub.docker.com/r/sonatype/nexus3>
- <https://hub.docker.com/r/klo2k/nexus3>

```shell
$ docker pull sonatype/nexus3:3.40.1
$ docker pull klo2k/nexus3:3.40.1-01

$ docker volume create --name nexus-data

$ docker run -d --name chaos-nexus \
    -p 8081:8081 \
    -e NEXUS_CONTEXT=nexus \
    -v nexus-data:/nexus-data \
    klo2k/nexus3:3.40.1-01
```

- <http://localhost:8081/nexus/> admin/admin@chaos

## 运维

```shell
$ docker logs -f chaos-nexus

# 停止服务
$ docker stop --time=120 chaos-nexus
```