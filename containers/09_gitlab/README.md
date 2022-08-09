# GitLab

<https://docs.gitlab.com/>

## docker 部署

- <https://hub.docker.com/r/gitlab/gitlab-ce>
- <https://docs.gitlab.com/ee/install/docker.html>
- <https://hub.docker.com/r/yrzr/gitlab-ce-arm64v8>

```shell
$ docker pull gitlab/gitlab-ce:15.2.0-ce.0
$ docker pull gitlab/gitlab-ce:14.10.5-ce.0
$ docker pull yrzr/gitlab-ce-arm64v8:14.10.5-ce.0

$ export GITLAB_HOME=/Users/zhangbaohao/workspace/vscode/dockers/containers/09_gitlab

$ docker volume create gitlab-logs
$ docker volume create gitlab-data

$ docker run -d --name chaos-gitlab \
    -p 8080:80 \
    -v $GITLAB_HOME/config:/etc/gitlab \
    -v gitlab-logs:/var/log/gitlab \
    -v gitlab-data:/var/opt/gitlab \
    --shm-size 256m \
    --privileged=true \
    yrzr/gitlab-ce-arm64v8:14.10.5-ce.0
```

- <http://localhost:8080> root/密码参见文件config/initial_root_password

## 关闭注册验证

- <http://localhost:8080/admin/application_settings/general>  Sign-up restrictions 取消勾选 Require admin approval for new sign-ups

## 头像配置优化

- <http://localhost:8080/admin/application_settings/general> Account and limit 取消勾选：Gravatar enabled