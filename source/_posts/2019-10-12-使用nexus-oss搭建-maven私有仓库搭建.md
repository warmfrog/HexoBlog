---
title: 使用nexus-oss搭建-maven私有仓库搭建
date: 2019-10-12 09:51:36
tags:
---

## 安装

[官方地址][0]

[0]: https://help.sonatype.com/repomanager3/installation/installation-methods

* 下载安装包

* 安装

`./nexus run`

* 登录

打开 <http://localhost:8081>,登录。

## 本地项目部署

### maven setting.xml 设置

* 增加服务器认证

``` XML
      <server>
            <id>local-nexus-release</id>
            <username>admin</username>
            <password>admin123</password>
        </server>
        <server>
            <id>local-nexus-snapshots</id>
            <username>admin</username>
            <password>admin123</password>
        </server>
```

* 增加镜像

``` XML
  <mirror>
        <id>local-nexus-releases</id>
        <mirrorOf>*</mirrorOf>
        <url>http://localhost:8081/repository/maven-releases/</url>
    </mirror>
    <mirror>
        <id>local-nexus-snapshots</id>
        <mirrorOf>*</mirrorOf>
        <url>http://localhost:8081/repository/maven-snapshots/</url>
    </mirror>
```

* 项目部署配置

``` XML
    <distributionManagement>
        <repository>
            <id>local-nexus-releases</id>
            <url>http://localhost:8081/repository/maven-releases/</url>
        </repository>
        <snapshotRepository>
            <id>local-nexus-snapshots</id>
            <url>http://localhost:8081/repository/maven-snapshots/</url>
        </snapshotRepository>
    </distributionManagement>
```

