###### docker login/logout 命令

```shell
#登录到一个镜像仓库
docker login [OPTIONS] [SERVER]

#登录到registry.fit2cloud.com镜像仓库，只有登录了 才能pull registry.fit2cloud.com上的私有镜像
eg: docker login -u root -p password registry.fit2cloud.com

#登出镜像仓库
docker logout [SERVER]

#登出镜像仓库registry.fit2cloud.com
eg: docker logout registry.fit2cloud.com
```

###### options

* **-u**:用户名
* **-p**:密码

