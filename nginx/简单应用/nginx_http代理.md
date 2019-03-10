#### 配置简单的http_web代理



```shell

#设定服务列表
upstream example_server {
    server example.com:8089;
}

#代理参数配置
proxy_connect_timeout 180;
    proxy_send_timeout 180;
    proxy_read_timeout 180;
    proxy_set_header Host $host;
    proxy_set_header X-Forwarder-For $remote_addr;

    #反向代理的路径（和upstream绑定），location 后面设置映射的路径
    location / {
        proxy_pass http://example__server;
    }



```

