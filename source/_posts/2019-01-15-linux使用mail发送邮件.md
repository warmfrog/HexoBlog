
---
layout: post
title: linux使用mail发送邮件
tags: [linux,mail]
---

## 安装

直接在命令行输入

    mail

提示

    Command 'mail' not found, but can be installed with:

    sudo apt install mailutils

安装

    sudo apt install mailutils

提示将会安装如下包

    The following NEW packages will be installed: guile-2.0-libs libgsasl7 libkyotocabinet16v5 libmailutils5 libntlm0 mailutils mailutils-common postfix

安装完成后，配置 /etc/mail.rc

    sudo vim /etc/mail.rc

添加以下内容:

    set from=xxx@163.com
    set smtp=stmp.163.com
    set smtp-auth-user=xxx@163.com
    set smtp-auth-password=xxx
    set smtp-auth=login

* from: 你的邮箱地址
* smtp-auth-password: 密码或授权码

保存退出

测试

    mail -s "hello from test" **@qq.com < ./test.txt

查看收件人邮箱，可以已收到邮件

### 发送带附件的邮件

    mail -s "主题" **@qq.com -A 附件 < 文件(邮件正文.txt)

### 更多命令

    mail --help

