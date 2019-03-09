###### docker logs 命令

```shell
#查看容器的日志
docker logs [OPTIONS] CONTAINER

eg: docker logs redis #查看容器redis的日志
    docker logs -f redis #查看容器redis的日志，实时输出
    docker logs -f --tail=10 redis #查看容器redis的日志，实时输出10行
```

###### options

* **-f**:跟踪日志输出
* **--tail**:仅列出最新的N条容器日志
* **-t**:显示时间戳
* **--since**:显示某个时间点开始的所有日志