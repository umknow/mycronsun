# mycronsun

#### 项目简介

使用环境：linux

这是一个cronsun快捷部署大礼包

使用到了etcd发现共享服务

#### 快捷部署说明

1、安装mongodb

2、将本项目clone到路径:  /usr/local/

3、指定ip启动etcd: ./etcd --listen-client-urls [http://0.0.0.0:2379](http://0.0.0.0:2379/) --advertise-client-urls [http://0.0.0.0:2379](http://0.0.0.0:2379/) --listen-peer-urls [http://0.0.0.0:2380](http://0.0.0.0:2380/)

4、启动cronweb:  /usr/local/mycronsun/cronsun-v0.3.4/cronweb -conf conf/base.json >> /dev/null 2>&1 &

5、局域环境内添加节点：
    将cronsun-v0.3.4下的conf和cronnode复制到目标节点服务路径：/usr/local/mycronsun/cronsun-v0.3.4/
    启动服务：/usr/local/mycronsun/cronsun-v0.3.4/cronnode -conf conf/base.json >> /dev/null 2>&1 &

6、访问管理平台：http://x.x.x.x:7079/ui/

备注：平台初始账号&密码: [admin@admin.com](mailto:admin@admin.com) & admin