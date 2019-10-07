
---
layout: post
title: Virtualbox中通过HostOnly方式搭建5台ubuntu虚拟机 
tags: [Virtualbox]
---

在Virtualbox中安装5台虚拟机，要求5台ubuntu 虚拟机能够相互ping通，并且可以访问外网。

5台虚拟机如果要相互ping通，则需要在同一个网段，并且与网关在同一个网段，网关设为相同的地址。我的虚拟机地址设置为

    主机node1 192.168.101.237
    主机node2 192.168.101.239
    主机node3 192.168.101.240
    主机node4 192.168.101.241
    主机node5 192.168.101.243

所有主机网管设置为 192.168.101.102， 即 VirtualBox Host-Only Ethernet Adapter 的IP 地址

安装虚拟机，配置网络连接方式为hostonly，5台虚拟机均选择网络适配器 VirtualBox Host-Only Ethernet Adapter. 在 win10 宿主机上对以太网进行共享，右击 *以太网* -> *属性* -> *共享* -> 勾选两个复选框，选择分享到 VirtualBox Host-Only Ethernet Adapter 网卡。

虚拟机安装完后，对每台虚拟机: 修改 /etc/network/interfaces.

首先，查看网卡名称

    ifconfig

我的为 enp0s3

修改 /etc/network/interfaces

    sudo vim /etc/network/interfaces

添加以下设置静态ip，网关设置为 VirtualBox Host-Only Ethernet Adapter 网卡的IP地址

    auto enp0s3
    iface enp0s3 inet static
    address 192.168.101.237
    netmask 255.255.255.0
    gateway 192.168.101.102

重启网卡

    /etc/init.d/networking restart

设置DNS

    sudo vim /etc/systemd/resolved.conf

修改DNS

    DNS=114.114.114.114

重启虚拟机
