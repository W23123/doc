###### docker build 命令 

```shell
#使用Dockerfile构建docker镜像	
docker build [OPTIONS] PATH | URL | -

    #使用当前目录的Dockerfile构建镜像，标签为registry.fit2cloud.com/example/image:1.0.0
eg: docker build -t registry.fit2cloud.com/example/image:1.0.0 .
    #使用URL github.com/creack/docker-firefox 的 Dockerfile 创建镜像
    docker build github.com/creack/docker-firefox
    #指定了Dockerfile路径
    docker build -t registry.fit2cloud.com/example/image:1.0.0 -f /home/Dockerfile
```



###### options

* **-f**:Dockerfile的路径

* **--rm**:设置镜像成功后删除中间容器

* **--tag, -t**：镜像的名字及标签，通常 name:tag 或者 name 格式；可以在一次构建中为一个镜像设置多个标签

  