
---
layout: post
title: 在WSL ubuntu 18.04下安装配置mysql数据库
tags: [mysql]
---

## 一步安装

```bash
sudo apt install mysql-server
```

## mysql服务器操作

* 查看状态

`sudo service mysql status`

* 停止mysql服务器

`sudo service mysql stop`

* 启动服务器

`sudo service mysql start`

切换到root用户,登录mysql控制台

`mysql`

* 创建用户

```sql
create user 'username'@'%' identified by 'password';
grant all on *.* to 'username'@'%';
```

