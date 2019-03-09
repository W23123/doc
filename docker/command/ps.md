###### docker ps命令

```shell
#列出容器列表
docker ps [OPTIONS]

eg:
   docker ps #列出运行中的容器
   docker ps -a #列出所有容器(包括为运行的)
   docke ps -l #显示最近创建的容器
   docker ps -n #显示最近创建的n个容器
   docker -aq #显示所有容器的ID
   docker stop $(docker ps -aq) #stop停止所有容器
   docker  rm $(docker ps -aq) #remove删除所有容器
   docker ps -f name=redis #列出name包含redis的容器
   docker ps -f name=mysql -q #显示出name包含redis容器的ID
```

###### options

* **-a**:显示所有容器，包括为运行的
* **-l**:显示最近创建的容器
* **-n**:显示最近创建的n个容器
* **-q**:只显示容器ID，或者说编号
* **-f**:添加过滤条件
* **-s**:文件总大小