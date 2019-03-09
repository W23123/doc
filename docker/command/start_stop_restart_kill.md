###### docker start/stop/restart/kill 命令

```shell
#启动一个或多个容器
docker start container 

eg:docker start mysql

#停止一个或多个容器，-t参数 在杀死容器之前等待的秒数，默认10s
docker stop container

eg:docker stop mysql

#重启一个或多个容器，-t参数 在杀死容器之前等待的秒数，默认10s
docker restart container

eg:docker -i 20 restart mysql
eg:docker restart mysql redis

#kill 也是停止一个或多个容器，没有等待时间。一般用来强行终止程序并实现快速停止容器(慎用)
docker kill -s KIll contaier

注：容器的名称也可以为容器ID，在一个环境里容器ID和name都是唯一的
```



