######  docker rmi命令

```shell
#移除本地一个或多个镜像
docker rmi [OPTIONS] IMAGE [IMAGE...]

#移除87027f890bd3 87027f890bd4镜像，可以用镜像ID 或hub.c.163.com/library/redis:1.0.1这种形式
#这移除2个镜像
eg: docker rmi 87027f890bd3 87027f890bd4
    docker rmi -f 87027f890bd3 #强制移除

```

###### options

* **-f**:强制移除

######  