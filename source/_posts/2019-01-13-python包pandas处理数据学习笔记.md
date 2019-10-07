
---
layout: post
title: python包pandas处理数据学习笔记 
tags: [python, pandas]
---

pandas 有两种数据结构： 序列(Series), 数据帧(DataFrame)。数据帧是序列的容器，序列是标量的容器。

    for col in df.columns:
        series = df[col]

## 10 Minutes to pandas

导入pandas

    import pandas as pd
    import numpy as np
    import matplotlib.pyplot as plt

### 创建数据对象

    s = pd.Series([1,3,5,np.nan,6,8])
    dates = pd.date_range('20130101', periods = 6)
    df = pd.DataFrame(np.random.randn(6,4), index=dates, columns = list('ABCD'))

### 查看数据

    df.head()
    df.tail(3)
    df.index
    df.columns
    df.values
    df.describe()
    df.T
    df.sort_index(axis=1, ascending=False)
    df.sort_values(by='B')

### 选择

    df['A']
    df[0:3]

#### 根据标签选择

    df.loc[dates[0]]
    df.loc[:,['A','B']]
    df.loc['20130102':'20130104', ['A','B']]
    df.loc['20130102',['A','B']]
    
* 获取标量值

    df.loc[date[0],'A']

* 更快的获取标量：

    df.at[dates[0],'A']

#### 根据位置选择

* 通过整数位置选择：

    df.iloc[3]

* 切片：

    df.iloc[3:5, 0:2]
    df.iloc[[1,2,4],[0,2]]
    df.iloc[1:3,:]
    df.iloc[:,1:3]
    df.iloc[1,1]

* 更快的获取标量:

    df.iat[1,1]

#### Boolean索引

    df[df.A > 0]
    df[df > 0]

* isin()方法过滤

    df2[df2['E'].isin(['two','four'])]

#### 设置

    s1 = pd.Series([1,2,3,4,5,6], index = pd.date_range('20130102', periods=6))
    df.at[dates[0],'A'] = 0
    df.iat[0,1] = 0
    df.loc[:,'D'] = np.array[5] * len(df))

* 拷贝

    df2 = df.copy()

#### 缺失的数据

    df1 = df.reindex(index = dates[0:4], columns = list(df.columns) + ['E'])
    df1.loc[dates[0]:dates[1], 'E'] = 1

* 丢弃遗失数据行

    df1.dropna(how = 'any')

* 填充缺失的数据

    df1.fillna(value=5)

* 是否为空

    pd.isna(df1)

### 操作

#### 统计

    df.mean()
    df.mean(1)

#### 应用

* 应用函数到数据 

    df.apply(np.cumsum)
    df.apply(lambda x: x.max() - x.min())

#### 合并

* 拼接

    pd.concat(pieces)

* Join

    pd.join(left,right, on = 'key')

* Merge

    pd.merge(left,right, on = 'key')

* Append

    df.append(s, ignore_index= True)

#### 分组 

    df.groupby(['A','B']).sum()

### 时间序列

    rng = pd.date_range('1/1/12012', period=100, freq='S')
    ts = pd.Series(np.random.randint(0,500, len(rng)), index = rng)

### 从输入输出获取数据

#### CSV

    df.to_csv('foo.csv')
    pd.read_csv('foo.csv')

#### HDF5

#### Excel

    df.to_excel('foo.xlsx', sheet_name='Sheet1')
    pd.read_excel('foo.xlsx', 'Sheet1', index_col=None, na_values=['NA'])

### Idioms

* if-then

    df.loc[df.AAA >= 5, 'BBB'] = -1; 
    df.loc[df.AAA >=5, ['BBB','CCC']] = 555;
    df.loc[df.AAA <5, ['BBB', 'CCC']] = 2000;

#### Splitting

    dflow = df[df.AAA <=5];
    dfhigh = df[df.AAA > 5];

#### 构建条件(Criteria)

    newseries = df.loc[(df['BBB'] < 25 & (df['CCC'] >= -40), 'AAA')];
    df.loc[(df['BBB'] > 25) | (df['CCC'] >= 75), 'AAA'] = 0.1;

    Crit1 = df.AAA <= 5.5
    Crit2 = df.BBB == 10.0
    Crit3 = df.CCC > -40.0
    AllCrit = Crit1 & Crit2 & Crit3
    CritList = [Crit1, Crit2, Crit3]
    AllCrit = functools.reduce(lambda x,y: x & y, CritList)
    df[AllCrit
    ]

## 必要的基础功能







