###### docker push命令

```shell
#docker 本地镜像push镜像到仓库，push之前要login 镜像仓库
docker push [OPTIONS] NAME[:TAG]

	# push 到registry.fit2cloud.com仓库
eg: docker push registry.fit2cloud.com/fit2cloud2/master/redis:1.2.0
	#push 到Docker Hub镜像仓库
    dcoker push redis:1.2.0
```

