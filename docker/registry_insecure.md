设置没有配置https的仓库地址

```shell
mac 界面上可以直接添加，然后重启

centos7

vi /etc/sysconfig/docker 

#配置一个或多个 非https仓库镜像地址
INSECURE_REGISTRY='--insecure-registry 10.XX.XX.XX:5000'
INSECURE_REGISTRY='--insecure-registry 10.XX.XX.XX:5000 --insecure-registry 10.XX.XX.XX:5000'

然后重启容器 systemctl restart docker
```

