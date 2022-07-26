# jenkins

<https://www.jenkins.io/>

## docker 部署

- <https://hub.docker.com/r/jenkins/jenkins>
- <https://github.com/jenkinsci/docker/blob/master/README.md>

```shell
$ docker pull jenkins/jenkins:lts-jdk11

$ export JENKINS_HOME=/Users/zhangbaohao/workspace/vscode/dockers/containers/08_jenkins

$ docker volume create jenkins-data

$ docker run -d --name chaos-jenkins \
    -p 8080:8080 \
    -p 50000:50000 \
    -e JENKINS_OPTS="--prefix=/jenkins" \
    -v jenkins-data:/var/jenkins_home \
    -v $JENKINS_HOME/software:/opt/local \
    jenkins/jenkins:lts-jdk11
```

## 初始化

<http://localhost:8080/jenkins> 25433e864b57408a9a4d7a44ac325e60

admin / admin@chaos

```shell
# java

# maven
# nodejs

```