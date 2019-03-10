#### NGINX 安装

环境：centos7.6 64bit

```shell
#安装
wget http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm

rpm -ivh nginx-release-centos-7-0.el7.ngx.noarch.rpm 

yum -y install nginx

#使用
nginx 启动
nginx -s stop 停止
nginx -t 测试配置文件是否正确
nginx -T 测试配置文件是否正确，并dump配置信息
nginx -s 发送一个信号 stop,quit,reload,reopen
nginx -c /home/nginx.conf 指定配置文件

```

