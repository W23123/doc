###### docker commit 命令

```shell
#从容器中创建一个新的镜像
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]

#将redis容器制作成registry.fit2cloud.com/example/redis:2.0.0镜像,registry.fit2cloud.com镜像仓库地址
docker commit -a "developer" -m "fix bug" redis registry.fit2cloud.com/example/redis:2.0.0

```



###### options

* -a:提交镜像的作者
* -m:提交信息
* -c:使用dockerfile指令来创建镜像
* -p:在commit时暂停容器

