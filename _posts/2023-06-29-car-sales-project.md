---
layout: post
title: "car-sales-project"
categories: project
author:
- Anis Taluqdar
meta: "Springfield"

jupyter:
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.10.9
  nbformat: 4
  nbformat_minor: 2
  orig_nbformat: 4
  vscode:
    interpreter:
      hash: 5c2dd6149c0277fc86f2b56d07fb350f55bdb295a29e1e4f8c4790fee70996c5
---

<div class="cell markdown">

1.  Problem definition
2.  Data
3.  Evaluation
4.  Features
5.  Modelling
6.  Experimentation

</div>

<div class="cell code" execution_count="30">

``` python
import pandas as pd
import matplotlib.pyplot as plt
```

</div>

<div class="cell code" execution_count="14">

``` python
df = pd.read_csv("E:\VSCode\zero-to-mastery-ml\data\car-sales-extended.csv")
```

</div>

<div class="cell code" execution_count="38">

``` python
df
```

<div class="output execute_result" execution_count="38">

           Make Colour  Odometer (KM)  Doors  Price
    0     Honda  White          35431      4  15323
    1       BMW   Blue         192714      5  19943
    2     Honda  White          84714      4  28343
    3    Toyota  White         154365      4  13434
    4    Nissan   Blue         181577      3  14043
    ..      ...    ...            ...    ...    ...
    995  Toyota  Black          35820      4  32042
    996  Nissan  White         155144      3   5716
    997  Nissan   Blue          66604      4  31570
    998   Honda  White         215883      4   4001
    999  Toyota   Blue         248360      4  12732

    [1000 rows x 5 columns]

</div>

</div>

<div class="cell code" execution_count="16">

``` python
df.info()
```

<div class="output stream stdout">

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 1000 entries, 0 to 999
    Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype 
    ---  ------         --------------  ----- 
     0   Make           1000 non-null   object
     1   Colour         1000 non-null   object
     2   Odometer (KM)  1000 non-null   int64 
     3   Doors          1000 non-null   int64 
     4   Price          1000 non-null   int64 
    dtypes: int64(3), object(2)
    memory usage: 39.2+ KB

</div>

</div>

<div class="cell code" execution_count="33">

``` python
df.isna().sum()
```

<div class="output execute_result" execution_count="33">

    Make             0
    Colour           0
    Odometer (KM)    0
    Doors            0
    Price            0
    dtype: int64

</div>

</div>

<div class="cell code" execution_count="36">

``` python
df.dtypes
```

<div class="output execute_result" execution_count="36">

    Make             object
    Colour           object
    Odometer (KM)     int64
    Doors             int64
    Price             int64
    dtype: object

</div>

</div>

<div class="cell code">

``` python
```

</div>
