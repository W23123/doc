

###### Docker run/create 命令

```shell
docker run/create [options] image [command] [arg...]

#create和run的区别是：create只创建容器不运行，run创建出容器并运行
```

###### options说明

- **-d**:后台运行容器，并返回容器ID
- **-i**:以交互模式运行容器，通常与 **-t** 一起使用
- **-t**:为容器重新分配一个伪输入终端，通常与 **-i**
- **-p**:端口映射，格式 **主机端口:容器端口**
- **-P**:将容器端口映射到主机的随机端口
- **--name**:指定容器名称
- **-h**:指定容器hostname
- **-e**:设置环境变量，如 -e MYSQL_ROOT_PASSWORD=dongbin
- **--env-file=[]**:从指定的文件读入环境变量
- **-m**:设置容器使用内存最大值
- **--link=[]**:添加链接到另一个容器
- **--expose=[]**:开放一个或一组端口
- **-v**:挂载目录，**主机文件目录:容器文件目录**。eg: -v /Users/dongbin/redis/backup/:/data

###### 示例

使用镜像**hub.c.163.com/library/redis:latest**以后台模式运行容器并且容器名为 **redis**

```properties
docker run -d --name=redis hub.c.163.com/library/redis:latest
```

使用镜像**hub.c.163.com/library/redis:latest**以后台模式运行容器，将Redis的默认端口6379映射到主机随机端口

```properties
docker run -d -P hub.c.163.com/library/redis:latest
```

使用镜像**hub.c.163.com/library/redis:latest**以后台模式运行容器，将Redis的默认端口6379映射到主机的端口56379

```properties
docker run -d -p 56379:6379 hub.c.163.com/library/redis:latest
```

使用镜像**hub.c.163.com/library/redis:latest**以后台模式运行容器，将Redis的默认端口6379映射到主机的端口56379，并且将主机的/Users/dongbin/redis/backup 目录映射到容器的/data (备份Redis)

```properties
docker run -d -p 56379:6379 -v /Users/dongbin/redis/backup:/data hub.c.163.com/library/redis:latest
```

使用镜像**hub.c.163.com/library/redis:latest**以交互模式启动一个容器，在容器内执行/bin/bash (进入容器里可以执行命令，容器退出时，当前容器停止)

```properties
docker run -it hub.c.163.com/library/redis:latest /bin/bash
```

