---
layout: post
title: "Pandas"
categories: Resources
author:
- Anis Taluqdar
meta: "Springfield"
---
    
    
# import pandas as pd
import pandas as pd 

# Creating a series of car types
cars = pd.Series(["BMW", "Toyota", "Honda"])
cars

0       BMW
1    Toyota
2     Honda
dtype: object

# Creating a series of colours
colours = pd.Series(["Blue", "Red", "White"])
colours

0     Blue
1      Red
2    White
dtype: object

# Creating a DataFrame of cars and colours
car_data = pd.DataFrame({"Car Type": cars,
"Colour": colours})

car_data

     Car Type Colour
0      BMW   Blue
1   Toyota    Red
2    Honda  White

# Create Series of food
foods = pd.Series(["Banana","Apple","Orange"])
foods

0    Banana
1     Apple
2    Orange
dtype: object

# Create Series of doller values
doller_values = pd.Series([4,5,7])
doller_values

0    4
1    5
2    7
dtype: int64

# Combine of foods and doller_values Create DataFrame of food_data
food_data = pd.DataFrame({"Food": foods,
"Price" : doller_values})

food_data

     Food  Price
0  Banana      4
1   Apple      5
2  Orange      7

# Example solution

# Make a Serise of different foods
foods = pd.Series(["Almond butter", "Eggs", "Avocado"])

# Make a Serise of different doller values
prices = pd.Series([9,6,2])

# Combine yuor Series of foods and doller values into a DataFrame

food_data = pd.DataFrame({"Foods": foods,
                              "Price" : prices})

food_data

               Foods  Price
0  Almond butter      9
1           Eggs      6
2        Avocado      2

# Import car sales data
car_sales = pd.read_csv("/home/anis/Documents/zero-to-mastery-ml/data/car-sales.csv") # takes a filename as string as input
car_sales

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00
5  Toyota  Green          99213      4   $4,500.00
6   Honda   Blue          45698      4   $7,500.00
7   Honda   Blue          54738      4   $7,000.00
8  Toyota  White          60000      4   $6,250.00
9  Nissan  White          31600      4   $9,700.00

# Import the car sales data and save it to df

df = pd.read_csv("/home/anis/Documents/zero-to-mastery-ml/data/car-sales.csv")
df

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00
5  Toyota  Green          99213      4   $4,500.00
6   Honda   Blue          45698      4   $7,500.00
7   Honda   Blue          54738      4   $7,000.00
8  Toyota  White          60000      4   $6,250.00
9  Nissan  White          31600      4   $9,700.00

# Export the car sales DataFrame to csv
car_sales.to_csv("/home/anis/Documents/zero-to-mastery-ml/data/exported-car-sales.csv")

# Import the data from heart-disease csv to df

df = pd.read_csv("/home/anis/Documents/zero-to-mastery-ml/data/heart-disease.csv")
df

     age  sex  cp  trestbps  chol  fbs  restecg  thalach  exang  oldpeak  \
0     63    1   3       145   233    1        0      150      0      2.3   
1     37    1   2       130   250    0        1      187      0      3.5   
2     41    0   1       130   204    0        0      172      0      1.4   
3     56    1   1       120   236    0        1      178      0      0.8   
4     57    0   0       120   354    0        1      163      1      0.6   
..   ...  ...  ..       ...   ...  ...      ...      ...    ...      ...   
298   57    0   0       140   241    0        1      123      1      0.2   
299   45    1   3       110   264    0        1      132      0      1.2   
300   68    1   0       144   193    1        1      141      0      3.4   
301   57    1   0       130   131    0        1      115      1      1.2   
302   57    0   1       130   236    0        0      174      0      0.0   

     slope  ca  thal  target  
0        0   0     1       1  
1        0   0     2       1  
2        2   0     2       1  
3        2   0     2       1  
4        2   0     2       1  
..     ...  ..   ...     ...  
298      1   0     3       0  
299      1   0     3       0  
300      1   2     3       0  
301      1   1     3       0  
302      1   1     2       0  

[303 rows x 14 columns]

# Export the data from df to csv
df.to_csv("/home/anis/Documents/zero-to-mastery-ml/data/exported-car-sales.csv")

# Importing heart-disease.csv
patient_data = pd.read_csv("/home/anis/Documents/zero-to-mastery-ml/data/heart-disease.csv")
patient_data

     age  sex  cp  trestbps  chol  fbs  restecg  thalach  exang  oldpeak  \
0     63    1   3       145   233    1        0      150      0      2.3   
1     37    1   2       130   250    0        1      187      0      3.5   
2     41    0   1       130   204    0        0      172      0      1.4   
3     56    1   1       120   236    0        1      178      0      0.8   
4     57    0   0       120   354    0        1      163      1      0.6   
..   ...  ...  ..       ...   ...  ...      ...      ...    ...      ...   
298   57    0   0       140   241    0        1      123      1      0.2   
299   45    1   3       110   264    0        1      132      0      1.2   
300   68    1   0       144   193    1        1      141      0      3.4   
301   57    1   0       130   131    0        1      115      1      1.2   
302   57    0   1       130   236    0        0      174      0      0.0   

     slope  ca  thal  target  
0        0   0     1       1  
1        0   0     2       1  
2        2   0     2       1  
3        2   0     2       1  
4        2   0     2       1  
..     ...  ..   ...     ...  
298      1   0     3       0  
299      1   0     3       0  
300      1   2     3       0  
301      1   1     3       0  
302      1   1     2       0  

[303 rows x 14 columns]

# Exporting the patient_data DataFrame to csv
patient_data.to_csv("/home/anis/Documents/zero-to-mastery-ml/data/exported-patient-data.csv")

car_sales

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00
5  Toyota  Green          99213      4   $4,500.00
6   Honda   Blue          45698      4   $7,500.00
7   Honda   Blue          54738      4   $7,000.00
8  Toyota  White          60000      4   $6,250.00
9  Nissan  White          31600      4   $9,700.00

car_sales.dtypes

Make             object
Colour           object
Odometer (KM)     int64
Doors             int64
Price            object
dtype: object

car_sales.describe()

          Odometer (KM)      Doors
count      10.000000  10.000000
mean    78601.400000   4.000000
std     61983.471735   0.471405
min     11179.000000   3.000000
25%     35836.250000   4.000000
50%     57369.000000   4.000000
75%     96384.500000   4.000000
max    213095.000000   5.000000

car_sales.info()

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10 entries, 0 to 9
Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype 
---  ------         --------------  ----- 
     0   Make           10 non-null     object
     1   Colour         10 non-null     object
     2   Odometer (KM)  10 non-null     int64 
     3   Doors          10 non-null     int64 
     4   Price          10 non-null     object
dtypes: int64(2), object(3)
memory usage: 528.0+ bytes

# Calling .mean() on a DataFrame
car_sales.mean()

/tmp/ipykernel_5006/1912059355.py:2: FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None') is deprecated; in a future version this will raise TypeError.  Select only valid columns before calling the reduction.
     car_sales.mean()

Odometer (KM)    78601.4
Doors                4.0
dtype: float64

# Calling .mean() on a Series

car_prices = pd.Series([3000,3500, 11250])
car_prices.mean()

5916.666666666667

# Calling .sum() on a DataFrame
car_sales.sum()

Make             ToyotaHondaToyotaBMWNissanToyotaHondaHondaToyo...
Colour               WhiteRedBlueBlackWhiteGreenBlueBlueWhiteWhite
Odometer (KM)                                               786014
Doors                                                           40
Price            $4,000.00$5,000.00$7,000.00$22,000.00$3,500.00...
dtype: object

# Calling .sum() on a Series
car_prices.sum()

17750

car_sales.columns

Index(['Make', 'Colour', 'Odometer (KM)', 'Doors', 'Price'], dtype='object')

# Save car_sales columns to a list 
car_columns = car_sales.columns
car_columns[0]

'Make'

car_sales.index

RangeIndex(start=0, stop=10, step=1)

len(car_sales)

10

# Show the first 5 rows of car_sales
car_sales.head()

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00

# Show the first 7 rows of car_sales
car_sales.head(7)

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00
5  Toyota  Green          99213      4   $4,500.00
6   Honda   Blue          45698      4   $7,500.00

# Show bottom 5 rows of car_sales
car_sales.tail()

     Make Colour  Odometer (KM)  Doors      Price
5  Toyota  Green          99213      4  $4,500.00
6   Honda   Blue          45698      4  $7,500.00
7   Honda   Blue          54738      4  $7,000.00
8  Toyota  White          60000      4  $6,250.00
9  Nissan  White          31600      4  $9,700.00

# Create a sample series 
animals = pd.Series(["cat", "dog", "bird", "snake","ox","lion"],
                    index=[0, 3, 9, 8, 67, 3])

animals

0       cat
3       dog
9      bird
8     snake
67       ox
3      lion
dtype: object

# Select all indexes with 3
animals.loc[3]

3     dog
3    lion
dtype: object

# Select index 9
animals.loc[9]

'bird'

car_sales

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00
5  Toyota  Green          99213      4   $4,500.00
6   Honda   Blue          45698      4   $7,500.00
7   Honda   Blue          54738      4   $7,000.00
8  Toyota  White          60000      4   $6,250.00
9  Nissan  White          31600      4   $9,700.00

# Select row at index 3
car_sales.loc[3]

Make                    BMW
Colour                Black
Odometer (KM)         11179
Doors                     5
Price            $22,000.00
Name: 3, dtype: object

animals

0       cat
3       dog
9      bird
8     snake
67       ox
3      lion
dtype: object

# Select row at position 3
animals.iloc[3]

'snake'

# Select row at position 3
car_sales.iloc[3]

Make                    BMW
Colour                Black
Odometer (KM)         11179
Doors                     5
Price            $22,000.00
Name: 3, dtype: object

# Get all rows up to positon 3
animals.iloc[:3]

0     cat
3     dog
9    bird
dtype: object

# Get all rows up to (and including) index 3
car_sales.loc[:3]

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00

# Select Make column
car_sales['Make']

0    Toyota
1     Honda
2    Toyota
3       BMW
4    Nissan
5    Toyota
6     Honda
7     Honda
8    Toyota
9    Nissan
Name: Make, dtype: object

# Select Colour column
car_sales['Colour']

0    White
1      Red
2     Blue
3    Black
4    White
5    Green
6     Blue
7     Blue
8    White
9    White
Name: Colour, dtype: object

# Select cars with over 100,00 on the Odometer
car_sales[car_sales["Odometer (KM)"] > 100000]

     Make Colour  Odometer (KM)  Doors      Price
0  Toyota  White         150043      4  $4,000.00
4  Nissan  White         213095      4  $3,500.00

# Select cars which are made by Toyota
car_sales[car_sales["Make"] == "Toyota"]

     Make Colour  Odometer (KM)  Doors      Price
0  Toyota  White         150043      4  $4,000.00
2  Toyota   Blue          32549      3  $7,000.00
5  Toyota  Green          99213      4  $4,500.00
8  Toyota  White          60000      4  $6,250.00

# Compare car Make with number of Doors
pd.crosstab(car_sales["Make"], car_sales["Doors"])

Doors   3  4  5
Make           
BMW     0  0  1
Honda   0  3  0
Nissan  0  2  0
Toyota  1  3  0

car_sales

     Make Colour  Odometer (KM)  Doors       Price
0  Toyota  White         150043      4   $4,000.00
1   Honda    Red          87899      4   $5,000.00
2  Toyota   Blue          32549      3   $7,000.00
3     BMW  Black          11179      5  $22,000.00
4  Nissan  White         213095      4   $3,500.00
5  Toyota  Green          99213      4   $4,500.00
6   Honda   Blue          45698      4   $7,500.00
7   Honda   Blue          54738      4   $7,000.00
8  Toyota  White          60000      4   $6,250.00
9  Nissan  White          31600      4   $9,700.00

# Group by the Make column and find the mean of the other columns
car_sales.groupby(["Make"]).mean()

          Odometer (KM)  Doors
Make                        
BMW      11179.000000   5.00
Honda    62778.333333   4.00
Nissan  122347.500000   4.00
Toyota   85451.250000   3.75

# Import matplotlib and tell Jupyter to show plots
import matplotlib.pyplot as plt 
%matplotlib inline

car_sales["Odometer (KM)"].plot()

<AxesSubplot:>

![](dd7b516ce4fff74b929cd01d506692d2d5505013.png)

car_sales["Odometer (KM)"].hist()

<AxesSubplot:>

![](b30e292e26073b64deb62fe6a55e2f141ff77a0b.png)

car_sales["Price"].plot()

---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
/home/anis/Documents/zero-to-mastery-ml/Exercise/Pandas/basic-pandas.ipynb Cell 52' in <cell line: 1>()
----> <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Pandas/basic-pandas.ipynb#ch0000051?line=0'>1</a> car_sales["Price"].plot()

File ~/.local/lib/python3.10/site-packages/pandas/plotting/_core.py:972, in PlotAccessor.__call__(self, *args, **kwargs)
     969             label_name = label_kw or data.columns
     970             data.columns = label_name
--> 972 return plot_backend.plot(data, kind=kind, **kwargs)

File ~/.local/lib/python3.10/site-packages/pandas/plotting/_matplotlib/__init__.py:71, in plot(data, kind, **kwargs)
     69         kwargs["ax"] = getattr(ax, "left_ax", ax)
     70 plot_obj = PLOT_CLASSES[kind](data, **kwargs)
---> 71 plot_obj.generate()
     72 plot_obj.draw()
     73 return plot_obj.result

File ~/.local/lib/python3.10/site-packages/pandas/plotting/_matplotlib/core.py:327, in MPLPlot.generate(self)
     325 def generate(self):
     326     self._args_adjust()
--> 327     self._compute_plot_data()
     328     self._setup_subplots()
     329     self._make_plot()

File ~/.local/lib/python3.10/site-packages/pandas/plotting/_matplotlib/core.py:506, in MPLPlot._compute_plot_data(self)
     504 # no non-numeric frames or series allowed
     505 if is_empty:
--> 506     raise TypeError("no numeric data to plot")
     508 self.data = numeric_data.apply(self._convert_to_ndarray)

TypeError: no numeric data to plot

car_sales.info()

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10 entries, 0 to 9
Data columns (total 5 columns):
     #   Column         Non-Null Count  Dtype 
---  ------         --------------  ----- 
     0   Make           10 non-null     object
     1   Colour         10 non-null     object
     2   Odometer (KM)  10 non-null     int64 
     3   Doors          10 non-null     int64 
     4   Price          10 non-null     object
dtypes: int64(2), object(3)
memory usage: 528.0+ bytes

# Cahnge Price column to integers
car_sales["Price"] = car_sales["Price"].str.replace("[\$\,\.]","").astype(int)

/tmp/ipykernel_5006/300190200.py:2: FutureWarning: The default value of regex will change from True to False in a future version.
     car_sales["Price"] = car_sales["Price"].str.replace("[\$\,\.]","").astype(int)

car_sales

     Make Colour  Odometer (KM)  Doors    Price
0  Toyota  White         150043      4   400000
1   Honda    Red          87899      4   500000
2  Toyota   Blue          32549      3   700000
3     BMW  Black          11179      5  2200000
4  Nissan  White         213095      4   350000
5  Toyota  Green          99213      4   450000
6   Honda   Blue          45698      4   750000
7   Honda   Blue          54738      4   700000
8  Toyota  White          60000      4   625000
9  Nissan  White          31600      4   970000

car_sales["Price"].plot()

<AxesSubplot:>

![](76e16b681603fdafebe6a3bc5417f72033d22ca0.png)

# Lower the Make column
car_sales["Make"].str.lower()

0    toyota
1     honda
2    toyota
3       bmw
4    nissan
5    toyota
6     honda
7     honda
8    toyota
9    nissan
Name: Make, dtype: object

# View top 5 rows, Make column not lowered
car_sales.head()

     Make Colour  Odometer (KM)  Doors    Price
0  Toyota  White         150043      4   400000
1   Honda    Red          87899      4   500000
2  Toyota   Blue          32549      3   700000
3     BMW  Black          11179      5  2200000
4  Nissan  White         213095      4   350000

# Set Make column to be lowered 
car_sales["Make"]  = car_sales["Make"].str.lower()
car_sales.head()

     Make Colour  Odometer (KM)  Doors    Price
0  toyota  White         150043      4   400000
1   honda    Red          87899      4   500000
2  toyota   Blue          32549      3   700000
3     bmw  Black          11179      5  2200000
4  nissan  White         213095      4   350000

# Import car sales data with missing values
car_sales_missing = pd.read_csv("/home/anis/Documents/zero-to-mastery-ml/data/car-sales-missing-data.csv")
car_sales_missing

     Make Colour  Odometer  Doors    Price
0  Toyota  White  150043.0    4.0   $4,000
1   Honda    Red   87899.0    4.0   $5,000
2  Toyota   Blue       NaN    3.0   $7,000
3     BMW  Black   11179.0    5.0  $22,000
4  Nissan  White  213095.0    4.0   $3,500
5  Toyota  Green       NaN    4.0   $4,500
6   Honda    NaN       NaN    4.0   $7,500
7   Honda   Blue       NaN    4.0      NaN
8  Toyota  White   60000.0    NaN      NaN
9     NaN  White   31600.0    4.0   $9,700

# Fill Odometer column missing values with mean
car_sales_missing["Odometer"].fillna(car_sales_missing["Odometer"].mean(),
                                        inplace=False) # inplace is set to False by default

0    150043.000000
1     87899.000000
2     92302.666667
3     11179.000000
4    213095.000000
5     92302.666667
6     92302.666667
7     92302.666667
8     60000.000000
9     31600.000000
Name: Odometer, dtype: float64

car_sales_missing

     Make Colour  Odometer  Doors    Price
0  Toyota  White  150043.0    4.0   $4,000
1   Honda    Red   87899.0    4.0   $5,000
2  Toyota   Blue       NaN    3.0   $7,000
3     BMW  Black   11179.0    5.0  $22,000
4  Nissan  White  213095.0    4.0   $3,500
5  Toyota  Green       NaN    4.0   $4,500
6   Honda    NaN       NaN    4.0   $7,500
7   Honda   Blue       NaN    4.0      NaN
8  Toyota  White   60000.0    NaN      NaN
9     NaN  White   31600.0    4.0   $9,700

# Fill the Odometer missing values to the mean with inplace=True
car_sales_missing["Odometer"].fillna(car_sales_missing["Odometer"].mean(),
                                        inplace=True)

car_sales_missing

     Make Colour       Odometer  Doors    Price
0  Toyota  White  150043.000000    4.0   $4,000
1   Honda    Red   87899.000000    4.0   $5,000
2  Toyota   Blue   92302.666667    3.0   $7,000
3     BMW  Black   11179.000000    5.0  $22,000
4  Nissan  White  213095.000000    4.0   $3,500
5  Toyota  Green   92302.666667    4.0   $4,500
6   Honda    NaN   92302.666667    4.0   $7,500
7   Honda   Blue   92302.666667    4.0      NaN
8  Toyota  White   60000.000000    NaN      NaN
9     NaN  White   31600.000000    4.0   $9,700

# Remove missing data
car_sales_missing.dropna()

     Make Colour       Odometer  Doors    Price
0  Toyota  White  150043.000000    4.0   $4,000
1   Honda    Red   87899.000000    4.0   $5,000
2  Toyota   Blue   92302.666667    3.0   $7,000
3     BMW  Black   11179.000000    5.0  $22,000
4  Nissan  White  213095.000000    4.0   $3,500
5  Toyota  Green   92302.666667    4.0   $4,500

car_sales_missing

     Make Colour       Odometer  Doors    Price
0  Toyota  White  150043.000000    4.0   $4,000
1   Honda    Red   87899.000000    4.0   $5,000
2  Toyota   Blue   92302.666667    3.0   $7,000
3     BMW  Black   11179.000000    5.0  $22,000
4  Nissan  White  213095.000000    4.0   $3,500
5  Toyota  Green   92302.666667    4.0   $4,500
6   Honda    NaN   92302.666667    4.0   $7,500
7   Honda   Blue   92302.666667    4.0      NaN
8  Toyota  White   60000.000000    NaN      NaN
9     NaN  White   31600.000000    4.0   $9,700

car_sales_missing.dropna(inplace=True)

car_sales_missing

     Make Colour       Odometer  Doors    Price
0  Toyota  White  150043.000000    4.0   $4,000
1   Honda    Red   87899.000000    4.0   $5,000
2  Toyota   Blue   92302.666667    3.0   $7,000
3     BMW  Black   11179.000000    5.0  $22,000
4  Nissan  White  213095.000000    4.0   $3,500
5  Toyota  Green   92302.666667    4.0   $4,500

# Create a column from a pandas Series
seats_column = pd.Series([5, 5, 5, 5, 5, 5, 5,5 ,5, 5])
car_sales["Seats"] = seats_column
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats
0  toyota  White         150043      4   400000      5
1   honda    Red          87899      4   500000      5
2  toyota   Blue          32549      3   700000      5
3     bmw  Black          11179      5  2200000      5
4  nissan  White         213095      4   350000      5
5  toyota  Green          99213      4   450000      5
6   honda   Blue          45698      4   750000      5
7   honda   Blue          54738      4   700000      5
8  toyota  White          60000      4   625000      5
9  nissan  White          31600      4   970000      5

# Create a column from a Python list
engine_size = [1.3, 2.0, 3.0, 4.2, 1.6, 1, 2.0, 2.3, 2.0, 3.0]
car_sales["Engine Size"] = engine_size
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size
0  toyota  White         150043      4   400000      5          1.3
1   honda    Red          87899      4   500000      5          2.0
2  toyota   Blue          32549      3   700000      5          3.0
3     bmw  Black          11179      5  2200000      5          4.2
4  nissan  White         213095      4   350000      5          1.6
5  toyota  Green          99213      4   450000      5          1.0
6   honda   Blue          45698      4   750000      5          2.0
7   honda   Blue          54738      4   700000      5          2.3
8  toyota  White          60000      4   625000      5          2.0
9  nissan  White          31600      4   970000      5          3.0

# Column from other columns
car_sales["Price per KM"] = car_sales["Price"] / car_sales["Odometer (KM)"]
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0  toyota  White         150043      4   400000      5          1.3   
1   honda    Red          87899      4   500000      5          2.0   
2  toyota   Blue          32549      3   700000      5          3.0   
3     bmw  Black          11179      5  2200000      5          4.2   
4  nissan  White         213095      4   350000      5          1.6   
5  toyota  Green          99213      4   450000      5          1.0   
6   honda   Blue          45698      4   750000      5          2.0   
7   honda   Blue          54738      4   700000      5          2.3   
8  toyota  White          60000      4   625000      5          2.0   
9  nissan  White          31600      4   970000      5          3.0   

     Price per KM  
0      2.665902  
1      5.688347  
2     21.506037  
3    196.797567  
4      1.642460  
5      4.535696  
6     16.412097  
7     12.788191  
8     10.416667  
9     30.696203  

# Column to all 1 value (number of wheels)
car_sales["Number of wheels"] = 4
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0  toyota  White         150043      4   400000      5          1.3   
1   honda    Red          87899      4   500000      5          2.0   
2  toyota   Blue          32549      3   700000      5          3.0   
3     bmw  Black          11179      5  2200000      5          4.2   
4  nissan  White         213095      4   350000      5          1.6   
5  toyota  Green          99213      4   450000      5          1.0   
6   honda   Blue          45698      4   750000      5          2.0   
7   honda   Blue          54738      4   700000      5          2.3   
8  toyota  White          60000      4   625000      5          2.0   
9  nissan  White          31600      4   970000      5          3.0   

     Price per KM  Number of wheels  
0      2.665902                 4  
1      5.688347                 4  
2     21.506037                 4  
3    196.797567                 4  
4      1.642460                 4  
5      4.535696                 4  
6     16.412097                 4  
7     12.788191                 4  
8     10.416667                 4  
9     30.696203                 4  

car_sales["Passed road safety"] = True
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0  toyota  White         150043      4   400000      5          1.3   
1   honda    Red          87899      4   500000      5          2.0   
2  toyota   Blue          32549      3   700000      5          3.0   
3     bmw  Black          11179      5  2200000      5          4.2   
4  nissan  White         213095      4   350000      5          1.6   
5  toyota  Green          99213      4   450000      5          1.0   
6   honda   Blue          45698      4   750000      5          2.0   
7   honda   Blue          54738      4   700000      5          2.3   
8  toyota  White          60000      4   625000      5          2.0   
9  nissan  White          31600      4   970000      5          3.0   

     Price per KM  Number of wheels  Passed road safety  
0      2.665902                 4                True  
1      5.688347                 4                True  
2     21.506037                 4                True  
3    196.797567                 4                True  
4      1.642460                 4                True  
5      4.535696                 4                True  
6     16.412097                 4                True  
7     12.788191                 4                True  
8     10.416667                 4                True  
9     30.696203                 4                True  

# Drop the Price per KM colmun
car_sales = car_sales.drop("Price per KM", axis=1)
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0  toyota  White         150043      4   400000      5          1.3   
1   honda    Red          87899      4   500000      5          2.0   
2  toyota   Blue          32549      3   700000      5          3.0   
3     bmw  Black          11179      5  2200000      5          4.2   
4  nissan  White         213095      4   350000      5          1.6   
5  toyota  Green          99213      4   450000      5          1.0   
6   honda   Blue          45698      4   750000      5          2.0   
7   honda   Blue          54738      4   700000      5          2.3   
8  toyota  White          60000      4   625000      5          2.0   
9  nissan  White          31600      4   970000      5          3.0   

     Number of wheels  Passed road safety  
0                 4                True  
1                 4                True  
2                 4                True  
3                 4                True  
4                 4                True  
5                 4                True  
6                 4                True  
7                 4                True  
8                 4                True  
9                 4                True  

# Sample car_sales
car_sales_sampled = car_sales.sample(frac=1)
car_sales_sampled

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
9  nissan  White          31600      4   970000      5          3.0   
5  toyota  Green          99213      4   450000      5          1.0   
4  nissan  White         213095      4   350000      5          1.6   
1   honda    Red          87899      4   500000      5          2.0   
0  toyota  White         150043      4   400000      5          1.3   
3     bmw  Black          11179      5  2200000      5          4.2   
8  toyota  White          60000      4   625000      5          2.0   
6   honda   Blue          45698      4   750000      5          2.0   
2  toyota   Blue          32549      3   700000      5          3.0   
7   honda   Blue          54738      4   700000      5          2.3   

     Number of wheels  Passed road safety  
9                 4                True  
5                 4                True  
4                 4                True  
1                 4                True  
0                 4                True  
3                 4                True  
8                 4                True  
6                 4                True  
2                 4                True  
7                 4                True  

# Reset the indexes of car_sales_sampled
car_sales_sampled.reset_index()

     index    Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0      9  nissan  White          31600      4   970000      5          3.0   
1      5  toyota  Green          99213      4   450000      5          1.0   
2      4  nissan  White         213095      4   350000      5          1.6   
3      1   honda    Red          87899      4   500000      5          2.0   
4      0  toyota  White         150043      4   400000      5          1.3   
5      3     bmw  Black          11179      5  2200000      5          4.2   
6      8  toyota  White          60000      4   625000      5          2.0   
7      6   honda   Blue          45698      4   750000      5          2.0   
8      2  toyota   Blue          32549      3   700000      5          3.0   
9      7   honda   Blue          54738      4   700000      5          2.3   

     Number of wheels  Passed road safety  
0                 4                True  
1                 4                True  
2                 4                True  
3                 4                True  
4                 4                True  
5                 4                True  
6                 4                True  
7                 4                True  
8                 4                True  
9                 4                True  

# Change the Odometer values from kilometers to miles
car_sales["Odometer (KM)"].apply(lambda x: x / 1.6)

0     93776.875
1     54936.875
2     20343.125
3      6986.875
4    133184.375
5     62008.125
6     28561.250
7     34211.250
8     37500.000
9     19750.000
Name: Odometer (KM), dtype: float64

car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0  toyota  White         150043      4   400000      5          1.3   
1   honda    Red          87899      4   500000      5          2.0   
2  toyota   Blue          32549      3   700000      5          3.0   
3     bmw  Black          11179      5  2200000      5          4.2   
4  nissan  White         213095      4   350000      5          1.6   
5  toyota  Green          99213      4   450000      5          1.0   
6   honda   Blue          45698      4   750000      5          2.0   
7   honda   Blue          54738      4   700000      5          2.3   
8  toyota  White          60000      4   625000      5          2.0   
9  nissan  White          31600      4   970000      5          3.0   

     Number of wheels  Passed road safety  
0                 4                True  
1                 4                True  
2                 4                True  
3                 4                True  
4                 4                True  
5                 4                True  
6                 4                True  
7                 4                True  
8                 4                True  
9                 4                True  

# Reassign the Odometer colmun to be miles insted of kilometers 
car_sales["Odometer (KM)"] = car_sales["Odometer (KM)"].apply(lambda x:x /1.6)
car_sales

     Make Colour  Odometer (KM)  Doors    Price  Seats  Engine Size  \
0  toyota  White      93776.875      4   400000      5          1.3   
1   honda    Red      54936.875      4   500000      5          2.0   
2  toyota   Blue      20343.125      3   700000      5          3.0   
3     bmw  Black       6986.875      5  2200000      5          4.2   
4  nissan  White     133184.375      4   350000      5          1.6   
5  toyota  Green      62008.125      4   450000      5          1.0   
6   honda   Blue      28561.250      4   750000      5          2.0   
7   honda   Blue      34211.250      4   700000      5          2.3   
8  toyota  White      37500.000      4   625000      5          2.0   
9  nissan  White      19750.000      4   970000      5          3.0   

     Number of wheels  Passed road safety  
0                 4                True  
1                 4                True  
2                 4                True  
3                 4                True  
4                 4                True  
5                 4                True  
6                 4                True  
7                 4                True  
8                 4                True  
9                 4                True  
