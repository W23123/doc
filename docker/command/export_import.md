###### docker  export/import命令

```shell
#docker 把容器打包成文件
docker export [OPTIONS] CONTAINER
options
  -o:将输入写入到文件
#把容器redis打包成文件redis.tar
eg: docker export -o redis.tar redis

#从文件中创建镜像
docker import [OPTIONS] file|URL|- [REPOSITORY[:TAG]]
options
   -c:应用docker指令创建镜像
   -m:提交的信息

#把redis.tar导入的本地镜像，标签为xxxxxxx/xxxx/redis:1.0.0
eg: docker import redis.tar xxxxxxx/xxxx/redis:1.0.0


 docker export/import 没有镜像的版本记录， 这是对对容器的。
```

