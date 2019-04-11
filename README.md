# mycronsun

#### 项目简介

使用环境：linux

这是一个cronsun快捷部署大礼包

使用到了etcd发现共享服务

#### 快捷部署说明

###### 1、安装mongodb

###### 2、将本项目clone到路径

​	 <u>/usr/local/</u>

###### 3、指定ip启动etcd

​	  <u><u>/usr/local/etcd-v3.3.10-linux-amd64/etcd --listen-client-urls [http://0.0.0.0:2379](http://0.0.0.0:2379/) --advertise-client-urls [http://0.0.0.0:2379](http://0.0.0.0:2379/) --listen-peer-urls [http://0.0.0.0:2380](http://0.0.0.0:2380/)</u>

###### 4、启动cronweb

​	<u>/usr/local/mycronsun/cronsun-v0.3.4/cronweb -conf conf/base.json >> /dev/null 2>&1 &</u>

###### 5、局域环境内添加节点

​	将cronsun-v0.3.4下的conf和cronnode复制到目标节点服务路径：<u>/usr/local/mycronsun/cronsun-v0.3.4/</u>

​	启动服务：<u>/usr/local/mycronsun/cronsun-v0.3.4/cronnode -conf conf/base.json >> /dev/null 2>&1 &</u>

###### 6、访问管理平台

​	<u>http://x.x.x.x:7079/ui/</u>

###### 备注：

​	平台初始账号&密码: [<u>admin@admin.com](mailto:admin@admin.com) & admin</u>