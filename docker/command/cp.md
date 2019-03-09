######  docker cp命令

```shell
#把容器中的目录SRC_PATH 拷贝到目标目录DEST_PATH 
docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH

#把目录SRC_PATH 拷贝到容器中的DEST_PATH目录
docker cp [OPTIONS] SRC_PATH CONTAINER:DEST_PATH

    #把本机的home目录拷贝到容器的/root目录下
eg: docker cp /home redis:/root
    #把本机的home目录下的test.sh文件拷贝到容器的/root目录下
    docker cp /home/test.sh redis:/root
    #把容器redis的/root目录拷贝到本机的/home目录下
    docker redis:/root   /home
    #把容器redis的/root目录下的test.sh文件拷贝到本机的/home目录下
    docker redis:/root/test.sh /home
```

