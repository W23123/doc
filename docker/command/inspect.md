###### docker inspect命令

```shell
#查看容器/镜像的元数据
docker inspect [OPTIONS] NAME|ID [NAME|ID...]

eg:
  docker inspect hub.c.163.com/library/redis #查看Redis镜像的元数据信息
  docker inspcet redis #查看容器redis的元数据信息
  
```

###### options

* **-f**:指定返回值的模板文件
* **-s**:显示总得文件大小
* **--type**:为指定类型返回JSON

