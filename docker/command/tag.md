###### docker tag 命令 

```shell
#标记本地镜像，将其归入某一仓库
docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]

#将本地镜像hub.c.163.com/library/redis:5.3.7标记为registry.fit2cloud.com/example/redis:10.0.1
#注意它们的镜像ID还是一样的
#docker push registry.fit2cloud.com/example/redis:10.0.1 就把redis放到了registry.fit2cloud.com仓库
eg: docker tag hub.c.163.com/library/redis:5.3.7 registry.fit2cloud.com/example/redis:10.0.1
```

