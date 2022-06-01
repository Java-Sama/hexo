---
title: 使用docker安装MySQL
date: 2022-06-01 15:59:08
tags: 
- docker
- mysql
---

## 什么是 MySQL？
MySQL是世界上最受欢迎的开源数据库。凭借其经过验证的性能，可靠性和易用性，MySQL已成为基于Web的应用程序的领先数据库选择，涵盖了从个人项目和网站，通过电子商务和信息服务，一直到包括Facebook，Twitter，YouTube，Yahoo！等在内的高端Web资产的整个范围。

有关MySQL Server和其他MySQL产品的更多信息和相关下载，请访问 www.mysql.com。

![mysql_logo 图标](https://raw.githubusercontent.com/docker-library/docs/c408469abbac35ad1e4a50a6618836420eb9502e/mysql/logo.png)


``` shell
docker run \
 -p 3306:3306 \                                           #端口映射
 --name mysql \                                           #容器名称
 --restart=always \                                       #重启
 -v $HOME/Documents/mysql/conf:/etc/mysql \
 -v $HOME/Documents/mysql/logs:/var/log/mysql \
 -v $HOME/Documents/mysql/data:/var/lib/mysql \
 -e MYSQL_ROOT_PASSWORD=root \
 -d mysql:5.7
```
