###### docker exec命令

```shell
#在容器中执行命令
docker exec [OPTIONS] CONTAINER COMMAND [ARG...]

eg：
  #在容器redis里执行容器内脚本/home/build.sh
  docker exec -it redis /bin/sh /home/build.sh
  
  #在容器redis里开启一个交互式终端
  docker exec -it redis /bin/sh
  

```



###### options

* **-d**:分离模式，后台运行
* **-i**:即使没有附加也能保持STDIN打开
* **-t**:分配一个伪终端

