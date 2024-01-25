---
title: Pandas 使用
date: 2020-05-19 22:41
author: WangYu
cover: false
tags:
- Pandas
categories:
- Python
---

# Pandas 使用

```python
import numpy as np
import pandas as pd 

csv_file = 'data.csv'
csv_data = pd.read_csv(csv_file,low_memory = False) #防止弹出警告

df = pd.DataFrame()
print(df.shape) # 查看数据维度
print(df.duplicated()) #查看重复值
print(pd.isnull(df)) #查看缺失值
#将NAN值替换为0 pd.fillna 填补缺失值 df.where()
df.where(df.notnull(),0) 
```

<!--more-->

## pandas绘图

```python
import pandas
import numpy as np
from pandas import Series,DataFrame
import matplotlib.pyplot as plt
import matplotlib
matplotlib.style.use('gplot')

```

```python
import pandas as pd
rng = pd.period_range('2016-03','2016-12',freq='M')
print(rng)

PeriodIndex(['2016-03', '2016-04', '2016-05', '2016-06', '2016-07', '2016-08',
             '2016-09', '2016-10', '2016-11', '2016-12'],
            dtype='period[M]', freq='M')
```



