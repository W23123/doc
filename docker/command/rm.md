###### docker rm命令

```shell
#移除一个或多个容器
docker rm [options] containers

eg: docker rm redis #移除已停止的容器redis
    docker rm -f redis #移除正在运行中的容器redis
    docker rm -vf redis #移除正在运行中的容器redis并去掉相关的卷
```

###### options

* **-f**:通过SIGKILL信号强制删除一个运行中的容器
* **-v**:删除与容器相关的卷
* **-l**:删除指定的链接