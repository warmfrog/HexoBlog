
---
layout: post
title: window10下WSL给ubuntu18.04安装xfce桌面环境
tags: [windows10,WSL,xfce4,linux,xrdp]
---

首先修改源为阿里云的源，参考这篇文章[wsl-linux-ubuntu18.04更换阿里云源](2019-01-20-wsl-linux-ubuntu18.04更换阿里云源)

    sudo apt install xrdp
    sudo apt install vnc4server
    sudo apt install xubuntu-desktop

修改端口3389，改为其他的
    sudo vi /etc/xrdp/xrdp.ini

启动

    echo xfce4-session > ~/.xsession
    sudo service xrdp restart

然后，就可以在windows下使用mstsc (Windows自带的远程桌面工具连接了localhost:修改的端口)