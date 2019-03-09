###### docker 镜像 image

```shell
docker 镜像的结构为  镜像仓库/目录…/镜像名称:镜像版本

# 在镜像仓库registry.fit2cloud.com 目录(项目)fit2cloud2/master 镜像redis 版本1.0.0
# docker pull 可以根据下面这个地址pull到镜像，如果这个镜像是私有的，需要docker login 仓库
eg： registry.fit2cloud.com/fit2cloud2/master/redis:1.0.0

#注：docker pull redis 是从Docker Hub的镜像仓库获取redis的latest(最新版本)
#    没写仓库地址，默认为Docker Hub的镜像仓库(公共的，国外)
#    没写镜像版本，默认获取最新的镜像版本latest(镜像仓库可能是1.0 或 2.0之类的 latest只是代表最新的)
    

```





