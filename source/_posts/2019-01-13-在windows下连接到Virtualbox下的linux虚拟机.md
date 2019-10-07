
---
layout: post
title: 在windows下连接到Virtualbox下的linux虚拟机 
tags: [ssh,windows,linux,Virtualbox]
---

## 通过ssh 连接 virtualbox 的ubuntu18

* 首先虚拟机要安装 openssh-server

进入ubuntu虚拟机terminal,输入:

    sudo apt install openssh-server

* ssh 连接虚拟机

    ssh root@192.168.101.236

## ubuntu 18.04.1 配置静态IP

在virtualbox 中配置虚拟机网卡为 host-only，选择一个virtualbox生成的网卡适配器,。

打开命令行terminal， 输入 ifconfig 查看网卡名称为 enp0s3， 编辑/etc/network/interfaces

    sudo vim /etc/network/interfaces

添加

    auto enp0s3
    iface enp0s3 inet static
    address 192.168.101.237
    netmask 255.255.255.0
    gateway 192.168.101.102

重启网卡

    /etc/init.d/networking restart

