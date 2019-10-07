
---
layout: post
title: window10下远程连接Linux桌面较好的一种方式 
tags: [windows10,linux]
---

linux 远程安装 vnc 服务器 x11vnc ，windows10 安装 UltraVNC Viewer 是一种不错的方式，并且都是免费的。

* 方式: linux 远程安装 *VNC* 服务器 *x11nvc*, window10 安装 UltraVNC Viewer

## Linux 安装vnc服务端

    sudo apt install x11vnc

启动

    x11vnc -passwd PASSWORD -display :0 -forever

停止

    x11vnc -remote stop

默认端口号为5590

## window 下安装 vnc 客户端访问linux桌面

* 安装 [ULtraVNC](http://www.uvnc.com/)

在 [官网](http://www.uvnc.com/)下载安装即可，安装成功后，在linux 服务端 vnc server 启动的情况下，访问下面地址即可连接，ipaddress为linux 服务端 *IP* 地址，

    ipaddress::5590

完成了上面，即大功告成了。

## linux 远程连接window10

Linux 安装 remmina, Remmina 同时支持 RDP 和 VNC 协议

    sudo apt install remmina

Windwo10 开启远程