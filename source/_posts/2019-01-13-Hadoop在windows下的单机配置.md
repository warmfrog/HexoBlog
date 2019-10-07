
---
layout: post
title: Hadoop在windows下的单机配置 
tags: [hadoop]
---

* hadoop home /D:/Env/hadoop-2.9.2

    vim D:/Env/hadoop-2.9.2/etc/hadoop/hadoop-env.cmd
    set JAVA_HOME=C:\PROGRA~1\Java\jdk1.8.0_171

## 配置伪分布式模式

* 修改hadoop-2.9.2\etc\hadoop\core-site.xml

```xml
     <configuration>
         <property>
         <!-- 定义了namenode的位置-->
             <name>fs.default.name</name>
             <value>hdfs://localhost:9000</value>
         </property>
       <property>
       <!-- 此目录为hdfs的根目录，存储的文件即存储在该目录 -->
         <name>hadoop.tmp.dir</name>
         <value>/D:/HDFS</value>
     </property>
     </configuration>
```

* 修改hadoop-2.9.2\etc\hadoop\hdfs-site.xml

```xml
     <configuration>
         <property>
         <!-- 定义数据复制的数量，1 表示复制 1份 -->
             <name>dfs.replication</name>
             <value>1</value>
         </property>
     </configuration>
```

* 修改hadoop-2.9.2\etc\hadoop\mapred-site.xml

```xml
    <?xml version="1.0"?>
    <?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
   
    <configuration>
        <property>
        <!-- 定义了JobTracker的位置-->
            <name>mapred.job.tracker</name>
            <value>localhost:9001</value>
        </property>
    </configuration>
```

    由于hadoop 在windows下运行需要winutil, 所以需要另外下载。下载[winutil](https://github.com/steveloughran/winutils), 将原hadoop 的bin 目录重命名为bin.bak， 将hadoop2.8.3/bin 目录复制到hadoop根目录。

### 启动hadoop

首次启动hadoop, 需要格式化hadoop将要用到的HDFS文件系统
* 格式化 NameNode
    hadoop namenode -format

* 启动 Hadoop

    start-dfs

* 终止 Hadoop

    stop-dfs

这会打开两个窗口，一个datanode, 一个namenode.

* 查看java 进程

    jps

* 查看文件系统

    hadoop fs -ls /

* 创建目录

    hadoop fs -mkdir /user

* 从本地拷贝文件

    hadoop fs -copyFromLocal test.txt /

* 文件拷贝

    hadoop fs -cp /test.txt /data

* 查看hdfs 文件内容

    hadoop fs -cat /test.txt

* 下载文件到本地

    hadoop fs -copyToLocal /text.txt

* 查看帮助

    hadoop fs -help

#### 网页查看 hadoop

    [localhost:50070](http://localhost:50070)
