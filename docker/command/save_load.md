###### docker sava/load命令

 ```shell
#docker 把镜像打成文件
docker save [OPTIONS] IMAGE [IMAGE...]
options
   -o:输出到文件
    
#把registry.fit2cloud.com/example/redis:1.0.0 打成redis.tar文件(就在当前目录下，ls能看见)
eg: docker save -o redis.tar registry.fit2cloud.com/example/redis:1.0.0
 
#docker 把文件导成镜像
docker load [OPTIONS]
options
   -i:从tar文件中读取
 
 #把redis.tar导成本地镜像，如果名称(标签)不对，可以用docker tag修改
 eg: docker load -i redis.tar
 
 docker save/load 保存的是当前版本有历史记录，即docker history IMAGE，有记录
 这个是针对镜像的
 
 ```

