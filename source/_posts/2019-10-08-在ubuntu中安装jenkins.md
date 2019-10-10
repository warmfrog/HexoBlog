---
title: 在ubuntu中安装jenkins
date: 2019-10-08 15:07:54
tags: [jenkins]
---

[官方指导安装][0]

``` bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
```

日志文件位置： /var/log/jenkins/jenkins.log

[0]: https://jenkins.io/zh/doc/book/installing/#debianubuntu
