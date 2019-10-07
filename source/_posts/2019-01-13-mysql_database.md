
---
layout: post
title: mysql_database 
tags: [mysql]
---

    create database ShareBook;
    use ShareBook;

## 笔记

### Mysql 查看帮助

    ? contents
    ? data types
    ? create
    ? create table
    ? int
    ? show

### 表修改

* 外键支持

mysql只有InnoDB 引擎支持外键，所以可以在建表最后添加 engine=InnoDB 来更改默认引擎，也可以通过修改： alter table user engine = innodb;然后通过下面代码增加约束

    alter table Admin add constraint foreign key (username) references User(username) on delete restrict on update cascade;

* 查看表的详细描述信息

    show create table user \G;

* unique 字段约束设置

    alter table user add unique(user_email);

* 添加外键约束

    alter table Admin add constraint foreign key (username) references User(username);

* 删除外键

    alter table user drop foreign key fk_user_1;

* 修改字段

    alter table user modify user_email varchar(21);

* 添加列

    alter table user add column age int(3);

* 删除字段

    alter table user drop column age;

* 字段改名

    alter table user change age age1 int(4);

* 修改字段顺序

    alter table user add birth date after ename;
    alter table user modify age int(3) first;

* 表改名

    alter table user rename users;

### 数据操作

#### 插入

* 插入多条记录

    insert into user (username,pswd)
    values
    ("warmfrog", "159491"),
    ("warmfrog2", "159492");

#### 更新

* 更新多表记录

    update user a, book b set a.username="warmfrog11", b.book_name="Software" where a.user_id=book.book_owner_id;

#### 查询

* 去重显示

    select distinct book_name from book;

* 排序

    select * from user order by user_id;

* 显示前3条记录

    select * from user order by user_id, register_time desc limit 3;

limit 和 order by 一起配合进行分页查询

#### 删除多条记录

    delete from User where username in ('warmfrog10','warmfrog9');

## 数据表

### user

   create table user(
        user_id bigint auto_increment,
        nickname varchar(20),
        password varchar(20),
        address varchar(50),
        register_time timestamp,
        phone_number varchar(11) unique,
        user_email varchar(20) unique,
        primary key (user_id)
    )engine=InnoDB character set=utf8;

### book

    create table book(
        book_id bigint auto_increment,
        order_id bigint,
        book_owner_id bigint,
        book_name varchar(30),
        book_author varchar(40),
        book_author2 varchar(40),
        book_translator varchar(40),
        book_intro varchar(500),
        book_publish_time timestamp,
        book_publisher varchar(20),
        book_edition tinyint,
        book_isbn varchar(20),
        book_rent_price float,
        book_buy_price float,
        foreign key(book_owner_id) references user(user_id) on delete cascade on update cascade,
        foreign key(order_id) references orders(order_id),
        primary key(book_id)
      )engine=InnoDB character set=utf8;

### orders

    create table orders(
        order_id bigint auto_increment,
        start_time timestamp,
        trade_type varchar(10),
        current_status varchar(10),
        deliver_id bigint,
        customer_id bigint,
        primary key(order_id)
      )engine=InnoDB character set=utf8;

### deliver

   create table deliver(
        deliver_id bigint auto_increment,
        deliver_order_id bigint,
        deliver_status varchar(10),
        deliver_method varchar(10),
        foreign key(deliver_order_id) references orders(order_id) on delete restrict on update cascade,
        primary key (deliver_id)
      )engine=InnoDB character set=utf8;
      
 [MySQL 8.0 Reference Manual](https://dev.mysql.com/doc/refman/8.0/en/)

## 数据库操作

#### 连接到数据库

     mysql -h localhost -u warmfrog -p
     
#### 查看数据库

     show databases;

     select database();

#### 使用数据库

     user test

#### 创建数据库

     create database *menagerie*;

## 表操作

#### [创建表](https://dev.mysql.com/doc/refman/8.0/en/creating-tables.html)

     create table pet (name varchar(20), owner varchar(20), species varchar(20), sex char(1), birth date, death date);

#### 查看表

     show tables;

#### 描述表信息

    describe pet;
    
## 数据操作

#### 将数据载入表

有如下数据，保存为 pet.txt. \N 表示 NULL. 数据之间以 tab 间隔.
**************************************************************
| name    | owner    | species    | sex    | birth    | death |                     
|--------|---------|--------|------------|---------|------|
|Fluffy  |  Harold  |  cat  |  f |   1993-02-04  |  \N   | 
|Claws |	Gwen |	cat |	m |	1994-03-17 |  \N |             
|Buffy |	Harold |	dog |	f |	1989-05-13 |  \N |
| Fang |	Benny |	dog |	m |	1990-08-27 | \N |
| Bowser |	Diane |	dog |	m |	1979-08-31 |	1995-07-29 |                 
| Chirpy |	Gwen |	bird |	f |	1998-09-11 |  \N |      
| Whistler |	Gwen |	bird |	\N |	  1997-12-09 |    \N |    
| Slim |	Benny |	snake |	m |	1996-04-29 |  \N       
************************************************************
#### 载入操作

    load data local infile /mnt/d/pet.txt into table pet;

#### 显示结果

     mysql> load data local infile '/root/pet.txt' into table pet;
     Query OK, 8 rows affected, 48 warnings (0.01 sec)
     Records: 8  Deleted: 0  Skipped: 0  Warnings: 48

#### 查看表中所有数据

     select * from pet;

#### 删除表中所有数据

     delete from pet;

## 数据查询

#### 单表查询

    1.  select * from pet where name = 'Bowser';
    
    2.  SELECT * FROM pet WHERE birth >= '1998-1-1';
     
    3.  SELECT * FROM pet WHERE species = 'dog' AND sex = 'f';
     
    4.  SELECT * FROM pet WHERE species = 'snake' OR species = 'bird';
     
    5.  SELECT * FROM pet WHERE (species = 'cat' AND sex = 'm') OR (species = 'dog' AND sex = 'f');

#### 选择特定列

    1.  SELECT name, birth FROM pet;
    
    2.  SELECT owner FROM pet;

#### 去重显示

    1.   SELECT DISTINCT owner FROM pet;

#### 按序显示

    1.  SELECT name, birth FROM pet ORDER BY birth;
    
    2.  SELECT name, birth FROM pet ORDER BY birth DESC;
    
    3.  SELECT name, species, birth FROM pet ORDER BY species, birth DESC;

#### 图案匹配

    ‘%’ 表示匹配任意数量的字符。
    
    1.  SELECT * FROM pet WHERE name LIKE 'b%';
    2.  SELECT * FROM pet WHERE name LIKE '%fy';
    3.  SELECT * FROM pet WHERE name LIKE '%w%';

    一个 ‘_' 表示一个字符，5个’_' 的字符 '_____' 表示仅仅匹配 5 个字符.
    
    4.  <SELECT * FROM pet WHERE name LIKE '_____';>

#### 正则匹配

    1.  . 匹配任意单个字符。
    2.  [...] 匹配方括号内的任意字符，[abc] 匹配 a, b, c.
    3.  * 表示匹配 0 个或 多个 * 之前的字符.
    4.  为了定位一个图案的开始和结束字符，^ 在开头， $ 在结尾.

    示例：
    
    1.  SELECT * FROM pet WHERE REGEXP_LIKE(name, '^b');
    
    2.  SELECT * FROM pet WHERE REGEXP_LIKE(name, '^b' COLLATE utf8mb4_0900_as_cs);
    
    3.  SELECT * FROM pet WHERE REGEXP_LIKE(name, BINARY '^b');
    
    4.  SELECT * FROM pet WHERE REGEXP_LIKE(name, '^b', 'c');
    
    5.  SELECT * FROM pet WHERE REGEXP_LIKE(name, 'fy$');
    
    6.  SELECT * FROM pet WHERE REGEXP_LIKE(name, 'w');
    
    7.  SELECT * FROM pet WHERE REGEXP_LIKE(name, '^.....$');    正好匹配5个字符.
    
    8.  SELECT * FROM pet WHERE REGEXP_LIKE(name, '^.{5}$');    同7.

## 计数

##### 查看有多少宠物

    1. SELECT COUNT(*) FROM pet;

##### 查看拥有宠物的人养了多少宠物

    2. SELECT owner, COUNT(*) FROM pet GROUP BY owner;

    3. SELECT species, COUNT(*) FROM pet GROUP BY species;

    4. SELECT sex, COUNT(*) FROM pet GROUP BY sex;

    5. SELECT species, sex, COUNT(*) FROM pet GROUP BY species, sex;

    6. SELECT species, sex, COUNT(*) FROM pet
       WHERE species = 'dog' OR species = 'cat'
       GROUP BY species, sex;

    7. SELECT species, sex, COUNT(*) FROM pet
    -> WHERE sex IS NOT NULL
    -> GROUP BY species, sex;

## 多表查询

#### [创建表 event](https://dev.mysql.com/doc/refman/8.0/en/multiple-tables.html)

    create table event (name varchar(20), date date, type varchar(15), remark varchar(255));

#### 载入下表数据

<table summary="pet record data that will appear in a tab delimited text file, as described in the preceding text."><col width="15%"><col width="15%"><col width="15%"><col width="35%"><thead><tr>
              <th scope="col">name</th>
              <th scope="col">date</th>
              <th scope="col">type</th>
              <th scope="col">remark</th>
            </tr></thead><tbody><tr>
              <td scope="row">Fluffy</td>
              <td>1995-05-15</td>
              <td>litter</td>
              <td>4 kittens, 3 female, 1 male</td>
            </tr><tr>
              <td scope="row">Buffy</td>
              <td>1993-06-23</td>
              <td>litter</td>
              <td>5 puppies, 2 female, 3 male</td>
            </tr><tr>
              <td scope="row">Buffy</td>
              <td>1994-06-19</td>
              <td>litter</td>
              <td>3 puppies, 3 female</td>
            </tr><tr>
              <td scope="row">Chirpy</td>
              <td>1999-03-21</td>
              <td>vet</td>
              <td>needed beak straightened</td>
            </tr><tr>
              <td scope="row">Slim</td>
              <td>1997-08-03</td>
              <td>vet</td>
              <td>broken rib</td>
            </tr><tr>
              <td scope="row">Bowser</td>
              <td>1991-10-12</td>
              <td>kennel</td>
              <td></td>
            </tr><tr>
              <td scope="row">Fang</td>
              <td>1991-10-12</td>
              <td>kennel</td>
              <td></td>
            </tr><tr>
              <td scope="row">Fang</td>
              <td>1998-08-28</td>
              <td>birthday</td>
              <td>Gave him a new chew toy</td>
            </tr><tr>
              <td scope="row">Claws</td>
              <td>1998-03-17</td>
              <td>birthday</td>
              <td>Gave him a new flea collar</td>
            </tr><tr>
              <td scope="row">Whistler</td>
              <td>1998-12-09</td>
              <td>birthday</td>
              <td>First birthday</td>
</tr></tbody></table>

    load data local infile '/root/event.txt' into table event;

#### 查询宠物年龄和家庭情况

    select pet.name,
    timestampdiff(year,birth,date) as age,
    remark
    from pet inner join event
    on pet.name = event.name
    where event.type = 'litter';












