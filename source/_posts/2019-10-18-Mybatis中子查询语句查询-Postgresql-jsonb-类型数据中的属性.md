---
title: Mybatis中子查询语句查询-Postgresql-jsonb-类型数据中的属性
date: 2019-10-18 14:32:40
tags:
---

Postgresql 的 jsonb 类型，官方文档中有很多相关函数和操作符，支持很多对 jsonb 数据类型的查询插入转换等操作。[官网地址][0]

其中 stations 是表 traffic_line 中的 jsonb 属性，格式如下：

``` json
[{
	"labels": ["label5", "label2"],
	"poiUuid": "967d40330ab74ceeb448327e9f3c1f9d",
	"latitude": "1100",
	"longitude": "2482",
	"stationName": "站点一"
}, {
	"labels": ["label3", "label4"],
	"poiUuid": "7de3dee663bd4bf5810f61a52603beca",
	"stationName": "站点二"
}]
```

下面是自己尝试的一些查询操作：

``` sql
select stations::jsonb from "tf".traffic_line;   --查询 stations 属性

select jsonb_array_length(stations::jsonb) from "tf".traffic_line;   --数组长度

select uuid, jsonb_array_elements(stations::jsonb)->'stationName' as station from "tf".traffic_line;   --查询 jsonb 数据中的 stationName 属性

-- 子查询，查询 traffic_line 表中所有 stationsName 像 '%站点一%' 的行。
select * from
(select
 	 *, jsonb_array_elements(stations)->>'stationName' like '%站点一%' as station
	 from "tf".traffic_line) as line
where station = true;

select uuid,jsonb_array_elements(stations::jsonb)->'stationName' as station from "tf".traffic_line;   --查询站点
select uuid,jsonb_typeof(jsonb_array_elements(stations::jsonb)->'stationName') from "tf".traffic_line;

-- ? 顶层是否包含对应 key
select stations->0?'stationName' from "tf".traffic_line;
select stations->0?'labels' from "tf".traffic_line;
select stations->0?'poiUuid' from "tf".traffic_line;

-- 选择数组的第一个元素
select stations::jsonb->0 from "tf".traffic_line;
select stations::jsonb->1 from "tf".traffic_line;


select stations::jsonb->0->'poiUuid' from "tf".traffic_line;
select stations::jsonb->0->'stationName' from "tf".traffic_line;

select stations::jsonb->0->'labels'->0 from "tf".traffic_line;

-- 判断包含关系
select stations::jsonb->0->'labels'@>'{"label1":1}' from "tf".traffic_line;

select stations->0->'labels' from "tf".traffic_line;            --["lable1:","label2"]
select stations->0->'labels'?'label1' from "tf".traffic_line;   --true
select stations->0->'labels'?'label' from "tf".traffic_line;    --false
```

[0]: https://www.postgresql.org/docs/10/functions-json.html