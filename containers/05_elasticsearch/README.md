# Elasticsearch

<https://www.elastic.co/cn/elasticsearch/>

## docker 部署

- <https://hub.docker.com/_/elasticsearch>
- <https://www.elastic.co/guide/en/elasticsearch/reference/7.17/docker.html>

```shell
$ docker pull elasticsearch:7.17.5

$ docker volume create elasticsearch-data

$ docker run -d --name chaos-elasticsearch \
	-p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -v elasticsearch-data:/usr/share/elasticsearch/data \
	elasticsearch:7.17.5
```
