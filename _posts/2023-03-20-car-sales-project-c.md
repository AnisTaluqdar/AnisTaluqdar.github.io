---
layout: post
title: "Car Sales Project C"
categories: Project
author:
- Anis Taluqdar
meta: "Springfield"
---


1.  Problem definition
2.  Data
3.  Evaluation
4.  Features
5.  Modelling
6.  Experimentation

    import pandas as pd
    
    import matplotlib.pyplot as plt

    df = pd.read_csv("E:\VSCode\zero-to-mastery-ml\data\car-sales-extended.csv")

    df

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

    df.info()

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

    df.isna().sum()

    Make             0

    Colour           0

    Odometer (KM)    0

    Doors            0

    Price            0

    dtype: int64

    df.dtypes

    Make             object

    Colour           object

    Odometer (KM)     int64

    Doors             int64

    Price             int64

    dtype: object
