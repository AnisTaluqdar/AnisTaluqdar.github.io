---
layout: post
title: "Data Science Roadmap3"
categories: Roadmap
author:
- Anis Taluqdar
meta: "Springfield"

jupyter:
  kernelspec:
    display_name: Python 3.10.4 64-bit
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
    version: 3.10.4
  nbformat: 4
  nbformat_minor: 2
  orig_nbformat: 4
  vscode:
    interpreter:
      hash: 916dbcbb3f70747c44a77c7bcd40155683ae19c65e1c03b4aa3499c5328201f1
---

::: {.cell .markdown}
## 0. Importing NumPy {#0-importing-numpy}
:::

::: {.cell .code execution_count="1"}
``` {.python}
# Import numpy
import numpy as np
```
:::

::: {.cell .markdown}
## 1. Data Types and attributes {#1-data-types-and-attributes}
:::

::: {.cell .code execution_count="6"}
``` {.python}
# 1-dimensonal array, also referrred to as a vector
a1 = np.array([1, 2, 3])

# 2-dimensional array, also referred to as matrix
a2 = np.array([[1, 3.0, 3.3],
                [2, 5, 6.5]])

# 3-diensional array, also referred to as a matrix
a3 = np.array([[[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]],
                [[10, 11, 12],
                [13, 14, 15],
                [16, 17, 18]]])
```
:::

::: {.cell .code execution_count="8"}
``` {.python}
a1.shape, a1.ndim, a1.dtype, a1.size, type(a1)
```

::: {.output .execute_result execution_count="8"}
    ((3,), 1, dtype('int64'), 3, numpy.ndarray)
:::
:::

::: {.cell .code execution_count="9"}
``` {.python}
a2.shape, a2.ndim, a2.dtype, a2.size, type(a2)
```

::: {.output .execute_result execution_count="9"}
    ((2, 3), 2, dtype('float64'), 6, numpy.ndarray)
:::
:::

::: {.cell .code execution_count="10"}
``` {.python}
a3.shape, a3.ndim, a3.dtype, a3.size, type(a3)
```

::: {.output .execute_result execution_count="10"}
    ((2, 3, 3), 3, dtype('int64'), 18, numpy.ndarray)
:::
:::

::: {.cell .code execution_count="11"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="11"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="12"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="12"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="13"}
``` {.python}
a3
```

::: {.output .execute_result execution_count="13"}
    array([[[ 1,  2,  3],
            [ 4,  5,  6],
            [ 7,  8,  9]],

           [[10, 11, 12],
            [13, 14, 15],
            [16, 17, 18]]])
:::
:::

::: {.cell .code execution_count="79"}
``` {.python}
import pandas as pd
df = pd.DataFrame(np.random.randint(10, size=(5, 3)),
                                    columns=["a","b","c"])
df
```

::: {.output .execute_result execution_count="79"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>a</th>
      <th>b</th>
      <th>c</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7</td>
      <td>8</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>9</td>
      <td>8</td>
    </tr>
    <tr>
      <th>2</th>
      <td>9</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>3</td>
      <td>5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>2</td>
      <td>3</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="17"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="17"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="20"}
``` {.python}
df2 = pd.DataFrame(a2)
df2
```

::: {.output .execute_result execution_count="20"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1.0</td>
      <td>3.0</td>
      <td>3.3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>5.0</td>
      <td>6.5</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .markdown}
## 2. Creating arrays {#2-creating-arrays}
:::

::: {.cell .code execution_count="22"}
``` {.python}
# Create a simple array
simple_array = np.array([1, 2, 3])
simple_array, simple_array.dtype
```

::: {.output .execute_result execution_count="22"}
    (array([1, 2, 3]), dtype('int64'))
:::
:::

::: {.cell .code execution_count="24"}
``` {.python}
simple_array = np.array((1,2,3))
simple_array, simple_array.dtype
```

::: {.output .execute_result execution_count="24"}
    (array([1, 2, 3]), dtype('int64'))
:::
:::

::: {.cell .code execution_count="31"}
``` {.python}
# Create an array of ones
ones = np.ones((10,2))
ones
```

::: {.output .execute_result execution_count="31"}
    array([[1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.],
           [1., 1.]])
:::
:::

::: {.cell .code execution_count="32"}
``` {.python}
# The default datatype is 'float64'
ones.dtype
```

::: {.output .execute_result execution_count="32"}
    dtype('float64')
:::
:::

::: {.cell .code execution_count="33"}
``` {.python}
# You can change the datatype with .astype()
ones.astype(int)
```

::: {.output .execute_result execution_count="33"}
    array([[1, 1],
           [1, 1],
           [1, 1],
           [1, 1],
           [1, 1],
           [1, 1],
           [1, 1],
           [1, 1],
           [1, 1],
           [1, 1]])
:::
:::

::: {.cell .code execution_count="35"}
``` {.python}
# Create an array of zeros
zeros = np.zeros((5, 3, 3))
zeros
```

::: {.output .execute_result execution_count="35"}
    array([[[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]],

           [[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]],

           [[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]],

           [[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]],

           [[0., 0., 0.],
            [0., 0., 0.],
            [0., 0., 0.]]])
:::
:::

::: {.cell .code execution_count="36"}
``` {.python}
zeros.dtype
```

::: {.output .execute_result execution_count="36"}
    dtype('float64')
:::
:::

::: {.cell .code execution_count="102"}
``` {.python}
# Create an array within a range of values
range_array = np.arange(0, 10, 2)

range_array
```

::: {.output .execute_result execution_count="102"}
    array([0, 2, 4, 6, 8])
:::
:::

::: {.cell .code execution_count="104"}
``` {.python}
# Random array
random_array = np.random.randint(10, size=(5,3))
random_array
```

::: {.output .execute_result execution_count="104"}
    array([[8, 1, 3],
           [3, 3, 7],
           [0, 1, 9],
           [9, 0, 4],
           [7, 3, 2]])
:::
:::

::: {.cell .code execution_count="45"}
``` {.python}
# Random array of floats (between 0 & 1)
np.random.random(size=(5, 3))
```

::: {.output .execute_result execution_count="45"}
    array([[0.75168092, 0.91702937, 0.41049918],
           [0.08590011, 0.01823349, 0.49933062],
           [0.88713741, 0.53487455, 0.38779697],
           [0.28596827, 0.6028908 , 0.80276038],
           [0.26449386, 0.53048788, 0.26040534]])
:::
:::

::: {.cell .code execution_count="46"}
``` {.python}
np.random.random((5,3))
```

::: {.output .execute_result execution_count="46"}
    array([[0.50327251, 0.29413096, 0.77165931],
           [0.70752844, 0.48932609, 0.03172852],
           [0.49918861, 0.15335161, 0.81236575],
           [0.95600881, 0.2869837 , 0.52006108],
           [0.10199367, 0.4872112 , 0.04241763]])
:::
:::

::: {.cell .code execution_count="47"}
``` {.python}
# Rnadom 5x3 array of floats (between 0 & 1), similar to above 
np.random.rand(5,3)
```

::: {.output .execute_result execution_count="47"}
    array([[0.37729635, 0.32031111, 0.43615939],
           [0.99417207, 0.9693227 , 0.99333376],
           [0.96333562, 0.51154883, 0.59323354],
           [0.34613776, 0.09798161, 0.70038891],
           [0.18361434, 0.81810236, 0.78600783]])
:::
:::

::: {.cell .code execution_count="48"}
``` {.python}
np.random.rand(5, 3)
```

::: {.output .execute_result execution_count="48"}
    array([[0.6657807 , 0.47084154, 0.78679921],
           [0.28354409, 0.1845852 , 0.41009468],
           [0.87283629, 0.17055242, 0.62885106],
           [0.71557414, 0.14880161, 0.74824883],
           [0.73168989, 0.5171756 , 0.71796175]])
:::
:::

::: {.cell .code execution_count="80"}
``` {.python}
# Ser random seed to 0
np.random.seed(0)

# Make 'random' numbers
np.random.randint(10, size=(5, 3))
```

::: {.output .execute_result execution_count="80"}
    array([[5, 0, 3],
           [3, 7, 9],
           [3, 5, 2],
           [4, 7, 6],
           [8, 8, 1]])
:::
:::

::: {.cell .code execution_count="81"}
``` {.python}
# Make more random numbers
np.random.randint(10, size=(5, 3))
```

::: {.output .execute_result execution_count="81"}
    array([[6, 7, 7],
           [8, 1, 5],
           [9, 8, 9],
           [4, 3, 0],
           [3, 5, 0]])
:::
:::

::: {.cell .code execution_count="82"}
``` {.python}
# Set random seed to same number as above
np.random.seed(0)

# The same random numbers come out 
np.random.randint(10, size=(5, 3))
```

::: {.output .execute_result execution_count="82"}
    array([[5, 0, 3],
           [3, 7, 9],
           [3, 5, 2],
           [4, 7, 6],
           [8, 8, 1]])
:::
:::

::: {.cell .code execution_count="83"}
``` {.python}
np.random.seed(0)
df = pd.DataFrame(np.random.randint(10, size=(5, 3)))
df
```

::: {.output .execute_result execution_count="83"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3</td>
      <td>7</td>
      <td>9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>7</td>
      <td>6</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8</td>
      <td>8</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="85"}
``` {.python}
a3
```

::: {.output .execute_result execution_count="85"}
    array([[[ 1,  2,  3],
            [ 4,  5,  6],
            [ 7,  8,  9]],

           [[10, 11, 12],
            [13, 14, 15],
            [16, 17, 18]]])
:::
:::

::: {.cell .code execution_count="89"}
``` {.python}
np.unique(a3)
```

::: {.output .execute_result execution_count="89"}
    array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16, 17,
           18])
:::
:::

::: {.cell .markdown}
## 3. Viewing arrays and matrices (indexing) {#3-viewing-arrays-and-matrices-indexing}
:::

::: {.cell .code execution_count="90"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="90"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="91"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="91"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="92"}
``` {.python}
a3
```

::: {.output .execute_result execution_count="92"}
    array([[[ 1,  2,  3],
            [ 4,  5,  6],
            [ 7,  8,  9]],

           [[10, 11, 12],
            [13, 14, 15],
            [16, 17, 18]]])
:::
:::

::: {.cell .code execution_count="93"}
``` {.python}
a1[0]
```

::: {.output .execute_result execution_count="93"}
    1
:::
:::

::: {.cell .code execution_count="94"}
``` {.python}
a2[0]
```

::: {.output .execute_result execution_count="94"}
    array([1. , 3. , 3.3])
:::
:::

::: {.cell .code execution_count="95"}
``` {.python}
a3[0]
```

::: {.output .execute_result execution_count="95"}
    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])
:::
:::

::: {.cell .code execution_count="96"}
``` {.python}
# Get 2nd row (index 1) of a2
a2[1]
```

::: {.output .execute_result execution_count="96"}
    array([2. , 5. , 6.5])
:::
:::

::: {.cell .code execution_count="109"}
``` {.python}
# Get the first 2 values of the first 2 rows of both arrays
a3[:2, :2, :2]
```

::: {.output .execute_result execution_count="109"}
    array([[[ 1,  2],
            [ 4,  5]],

           [[10, 11],
            [13, 14]]])
:::
:::

::: {.cell .code execution_count="110"}
``` {.python}
a4 = np.random.randint(10, size=(2, 3, 4, 5))
a4
```

::: {.output .execute_result execution_count="110"}
    array([[[[6, 7, 7, 8, 1],
             [5, 9, 8, 9, 4],
             [3, 0, 3, 5, 0],
             [2, 3, 8, 1, 3]],

            [[3, 3, 7, 0, 1],
             [9, 9, 0, 4, 7],
             [3, 2, 7, 2, 0],
             [0, 4, 5, 5, 6]],

            [[8, 4, 1, 4, 9],
             [8, 1, 1, 7, 9],
             [9, 3, 6, 7, 2],
             [0, 3, 5, 9, 4]]],


           [[[4, 6, 4, 4, 3],
             [4, 4, 8, 4, 3],
             [7, 5, 5, 0, 1],
             [5, 9, 3, 0, 5]],

            [[0, 1, 2, 4, 2],
             [0, 3, 2, 0, 7],
             [5, 9, 0, 2, 7],
             [2, 9, 2, 3, 3]],

            [[2, 3, 4, 1, 2],
             [9, 1, 4, 6, 8],
             [2, 3, 0, 0, 6],
             [0, 6, 3, 3, 8]]]])
:::
:::

::: {.cell .code execution_count="111"}
``` {.python}
a4.shape
```

::: {.output .execute_result execution_count="111"}
    (2, 3, 4, 5)
:::
:::

::: {.cell .code execution_count="119"}
``` {.python}
# Get only the first 4 numbers of each single vector
a4[:, :, :, :]
```

::: {.output .execute_result execution_count="119"}
    array([[[[6, 7, 7, 8, 1],
             [5, 9, 8, 9, 4],
             [3, 0, 3, 5, 0],
             [2, 3, 8, 1, 3]],

            [[3, 3, 7, 0, 1],
             [9, 9, 0, 4, 7],
             [3, 2, 7, 2, 0],
             [0, 4, 5, 5, 6]],

            [[8, 4, 1, 4, 9],
             [8, 1, 1, 7, 9],
             [9, 3, 6, 7, 2],
             [0, 3, 5, 9, 4]]],


           [[[4, 6, 4, 4, 3],
             [4, 4, 8, 4, 3],
             [7, 5, 5, 0, 1],
             [5, 9, 3, 0, 5]],

            [[0, 1, 2, 4, 2],
             [0, 3, 2, 0, 7],
             [5, 9, 0, 2, 7],
             [2, 9, 2, 3, 3]],

            [[2, 3, 4, 1, 2],
             [9, 1, 4, 6, 8],
             [2, 3, 0, 0, 6],
             [0, 6, 3, 3, 8]]]])
:::
:::

::: {.cell .markdown}
## 4. Manipulating and comparying arrays {#4-manipulating-and-comparying-arrays}
:::

::: {.cell .code execution_count="120"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="120"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="7"}
``` {.python}
ones = np.ones(3)
ones
```

::: {.output .execute_result execution_count="7"}
    array([1., 1., 1.])
:::
:::

::: {.cell .code execution_count="122"}
``` {.python}
# Add two arrays
a1 + ones
```

::: {.output .execute_result execution_count="122"}
    array([2., 3., 4.])
:::
:::

::: {.cell .code execution_count="123"}
``` {.python}
# Subtract two array
a1 - ones
```

::: {.output .execute_result execution_count="123"}
    array([0., 1., 2.])
:::
:::

::: {.cell .code execution_count="124"}
``` {.python}
# Multiply two arrays
a1 * ones
```

::: {.output .execute_result execution_count="124"}
    array([1., 2., 3.])
:::
:::

::: {.cell .code execution_count="127"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="127"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="128"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="128"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="125"}
``` {.python}
# Multiply two arrays
a1 * a2
```

::: {.output .execute_result execution_count="125"}
    array([[ 1. ,  6. ,  9.9],
           [ 2. , 10. , 19.5]])
:::
:::

::: {.cell .code execution_count="130"}
``` {.python}
a1.shape, a2.shape , a3.shape
```

::: {.output .execute_result execution_count="130"}
    ((3,), (2, 3), (2, 3, 3))
:::
:::

::: {.cell .code execution_count="131"}
``` {.python}
a2 * a3
```

::: {.output .error ename="ValueError" evalue="operands could not be broadcast together with shapes (2,3) (2,3,3) "}
    ---------------------------------------------------------------------------
    ValueError                                Traceback (most recent call last)
    /home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb Cell 56' in <cell line: 1>()
    ----> <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000059?line=0'>1</a> a2 * a3

    ValueError: operands could not be broadcast together with shapes (2,3) (2,3,3) 
:::
:::

::: {.cell .code execution_count="132"}
``` {.python}
a3
```

::: {.output .execute_result execution_count="132"}
    array([[[ 1,  2,  3],
            [ 4,  5,  6],
            [ 7,  8,  9]],

           [[10, 11, 12],
            [13, 14, 15],
            [16, 17, 18]]])
:::
:::

::: {.cell .code execution_count="133"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="133"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="134"}
``` {.python}
a1.shape
```

::: {.output .execute_result execution_count="134"}
    (3,)
:::
:::

::: {.cell .code execution_count="135"}
``` {.python}
a2.shape
```

::: {.output .execute_result execution_count="135"}
    (2, 3)
:::
:::

::: {.cell .code execution_count="136"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="136"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="3"}
``` {.python}
a1 + a2
```

::: {.output .execute_result execution_count="3"}
    array([[2. , 5. , 6.3],
           [3. , 7. , 9.5]])
:::
:::

::: {.cell .code execution_count="4"}
``` {.python}
a2 + 2
```

::: {.output .execute_result execution_count="4"}
    array([[3. , 5. , 5.3],
           [4. , 7. , 8.5]])
:::
:::

::: {.cell .code execution_count="5"}
``` {.python}
# Raies an error brcause there's a shape mismatch
a2 + a3
```

::: {.output .error ename="ValueError" evalue="operands could not be broadcast together with shapes (2,3) (2,3,3) "}
    ---------------------------------------------------------------------------
    ValueError                                Traceback (most recent call last)
    /home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb Cell 64' in <cell line: 2>()
          <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000063?line=0'>1</a> # Raies an error brcause there's a shape mismatch
    ----> <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000063?line=1'>2</a> a2 + a3

    ValueError: operands could not be broadcast together with shapes (2,3) (2,3,3) 
:::
:::

::: {.cell .code execution_count="8"}
``` {.python}
# Divide two arrayes
a1 / ones
```

::: {.output .execute_result execution_count="8"}
    array([1., 2., 3.])
:::
:::

::: {.cell .code execution_count="9"}
``` {.python}
# Divide using floor division
a2 // a1
```

::: {.output .execute_result execution_count="9"}
    array([[1., 1., 1.],
           [2., 2., 2.]])
:::
:::

::: {.cell .code execution_count="10"}
``` {.python}
# Take an array to a power 
a1 ** 2
```

::: {.output .execute_result execution_count="10"}
    array([1, 4, 9])
:::
:::

::: {.cell .code execution_count="11"}
``` {.python}
# You can also use np.square()
np.square(a1)
```

::: {.output .execute_result execution_count="11"}
    array([1, 4, 9])
:::
:::

::: {.cell .code execution_count="12"}
``` {.python}
# Modulus divide (What's the remainder)
a1 % 2
```

::: {.output .execute_result execution_count="12"}
    array([1, 0, 1])
:::
:::

::: {.cell .code execution_count="13"}
``` {.python}
# Find the log of an array
np.log(a1)
```

::: {.output .execute_result execution_count="13"}
    array([0.        , 0.69314718, 1.09861229])
:::
:::

::: {.cell .code execution_count="14"}
``` {.python}
# Find the exponential of an array
np.exp(a1)
```

::: {.output .execute_result execution_count="14"}
    array([ 2.71828183,  7.3890561 , 20.08553692])
:::
:::

::: {.cell .markdown}
## Aggregation
:::

::: {.cell .code execution_count="15"}
``` {.python}
sum(a1)
```

::: {.output .execute_result execution_count="15"}
    6
:::
:::

::: {.cell .code execution_count="16"}
``` {.python}
np.sum(a1)
```

::: {.output .execute_result execution_count="16"}
    6
:::
:::

::: {.cell .code execution_count="25"}
``` {.python}
massive_array = np.random.random(100000)
massive_array.size
```

::: {.output .execute_result execution_count="25"}
    100000
:::
:::

::: {.cell .code execution_count="22"}
``` {.python}
%timeit sum(massive_array) # Python sum()
```

::: {.output .stream .stdout}
    8.73 ms ± 130 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
:::
:::

::: {.cell .code execution_count="23"}
``` {.python}
%timeit np.sum(massive_array) # NumPy np.sum()
```

::: {.output .stream .stdout}
    45.6 µs ± 3.75 µs per loop (mean ± std. dev. of 7 runs, 10,000 loops each)
:::
:::

::: {.cell .code execution_count="26"}
``` {.python}
import random
massive_list = [random.randint(0, 10) for i in range(100000)]
len(massive_list)
```

::: {.output .execute_result execution_count="26"}
    100000
:::
:::

::: {.cell .code execution_count="27"}
``` {.python}
massive_list[:10]
```

::: {.output .execute_result execution_count="27"}
    [3, 10, 2, 6, 10, 7, 9, 0, 4, 5]
:::
:::

::: {.cell .code execution_count="29"}
``` {.python}
%timeit sum(massive_list)
```

::: {.output .stream .stdout}
    623 µs ± 23.6 µs per loop (mean ± std. dev. of 7 runs, 1,000 loops each)
:::
:::

::: {.cell .code execution_count="30"}
``` {.python}
%timeit np.sum(massive_list)
```

::: {.output .stream .stdout}
    7.68 ms ± 103 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
:::
:::

::: {.cell .code execution_count="31"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="31"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="32"}
``` {.python}
# Find the mean
np.mean(a2)
```

::: {.output .execute_result execution_count="32"}
    3.466666666666667
:::
:::

::: {.cell .code execution_count="33"}
``` {.python}
# Find the max 
np.max(a2)
```

::: {.output .execute_result execution_count="33"}
    6.5
:::
:::

::: {.cell .code execution_count="34"}
``` {.python}
# Find the min
np.min(a2)
```

::: {.output .execute_result execution_count="34"}
    1.0
:::
:::

::: {.cell .code execution_count="35"}
``` {.python}
# FInd the standard deviation
np.std(a2)
```

::: {.output .execute_result execution_count="35"}
    1.827262676488766
:::
:::

::: {.cell .code execution_count="37"}
``` {.python}
# Find the variance
np.var(a2)
```

::: {.output .execute_result execution_count="37"}
    3.3388888888888886
:::
:::

::: {.cell .code execution_count="38"}
``` {.python}
# The standard deviation is the square root of the variance 
np.sqrt(np.var(a2))
```

::: {.output .execute_result execution_count="38"}
    1.827262676488766
:::
:::

::: {.cell .code execution_count="39"}
``` {.python}
# Demo of variance
high_var_array = np.array([1, 100, 200, 300, 4000, 5000])
low_var_array = np.array([2, 4, 6, 8, 10])

np.var(high_var_array), np.var(low_var_array)
```

::: {.output .execute_result execution_count="39"}
    (4296133.472222221, 8.0)
:::
:::

::: {.cell .code execution_count="40"}
``` {.python}
np.std(high_var_array), np.std(low_var_array)
```

::: {.output .execute_result execution_count="40"}
    (2072.711623024829, 2.8284271247461903)
:::
:::

::: {.cell .code execution_count="48"}
``` {.python}
# The standard deviation is the square root of the variance
np.sqrt(np.var(high_var_array)), np.sqrt(np.var(low_var_array))
```

::: {.output .execute_result execution_count="48"}
    (2072.711623024829, 2.8284271247461903)
:::
:::

::: {.cell .code execution_count="49"}
``` {.python}
%matplotlib inline 
import matplotlib.pyplot as plt
plt.hist(high_var_array)
plt.show()
```

::: {.output .display_data}
![](vertopal_e5ff4a0f2525498f80074fb006aa87b6/bc5be2353a0f779681bbc6f32cd7b2445fff7311.png)
:::
:::

::: {.cell .code execution_count="50"}
``` {.python}
plt.hist(low_var_array)
plt.show()
```

::: {.output .display_data}
![](vertopal_e5ff4a0f2525498f80074fb006aa87b6/d9fea54825e32df7cc527d631daeeec2f10c170b.png)
:::
:::

::: {.cell .markdown}
## Reshaping
:::

::: {.cell .code execution_count="51"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="51"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="52"}
``` {.python}
a2.shape
```

::: {.output .execute_result execution_count="52"}
    (2, 3)
:::
:::

::: {.cell .code execution_count="53"}
``` {.python}
a2 + a3
```

::: {.output .error ename="ValueError" evalue="operands could not be broadcast together with shapes (2,3) (2,3,3) "}
    ---------------------------------------------------------------------------
    ValueError                                Traceback (most recent call last)
    /home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb Cell 97' in <cell line: 1>()
    ----> <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000097?line=0'>1</a> a2 + a3

    ValueError: operands could not be broadcast together with shapes (2,3) (2,3,3) 
:::
:::

::: {.cell .code execution_count="54"}
``` {.python}
a2.reshape(2, 3, 1)
```

::: {.output .execute_result execution_count="54"}
    array([[[1. ],
            [3. ],
            [3.3]],

           [[2. ],
            [5. ],
            [6.5]]])
:::
:::

::: {.cell .code execution_count="55"}
``` {.python}
a2.reshape(2, 3, 1) + a3
```

::: {.output .execute_result execution_count="55"}
    array([[[ 2. ,  3. ,  4. ],
            [ 7. ,  8. ,  9. ],
            [10.3, 11.3, 12.3]],

           [[12. , 13. , 14. ],
            [18. , 19. , 20. ],
            [22.5, 23.5, 24.5]]])
:::
:::

::: {.cell .markdown}
## Transpose
:::

::: {.cell .code execution_count="60"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="60"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="61"}
``` {.python}
a2.shape
```

::: {.output .execute_result execution_count="61"}
    (2, 3)
:::
:::

::: {.cell .code execution_count="62"}
``` {.python}
a2.T
```

::: {.output .execute_result execution_count="62"}
    array([[1. , 2. ],
           [3. , 5. ],
           [3.3, 6.5]])
:::
:::

::: {.cell .code execution_count="63"}
``` {.python}
a2.T.shape
```

::: {.output .execute_result execution_count="63"}
    (3, 2)
:::
:::

::: {.cell .code execution_count="64"}
``` {.python}
matrix = np.random.random(size=(5,3,3))
matrix
```

::: {.output .execute_result execution_count="64"}
    array([[[0.42993897, 0.7932152 , 0.79249832],
            [0.38412458, 0.73642304, 0.66064956],
            [0.87189511, 0.32849003, 0.35192549]],

           [[0.69747447, 0.34484073, 0.29956046],
            [0.42253008, 0.49339807, 0.61384741],
            [0.36347656, 0.08451965, 0.98961731]],

           [[0.50501692, 0.85767667, 0.25910572],
            [0.72526108, 0.1555424 , 0.73513558],
            [0.8511059 , 0.36938592, 0.88115493]],

           [[0.06255893, 0.42652878, 0.74055872],
            [0.55720578, 0.12500141, 0.42477618],
            [0.54939943, 0.47934803, 0.65861762]],

           [[0.75110428, 0.69521324, 0.72708953],
            [0.01352319, 0.57821728, 0.71570312],
            [0.61046013, 0.4260779 , 0.72351593]]])
:::
:::

::: {.cell .code execution_count="65"}
``` {.python}
matrix.shape
```

::: {.output .execute_result execution_count="65"}
    (5, 3, 3)
:::
:::

::: {.cell .code execution_count="66"}
``` {.python}
matrix.T
```

::: {.output .execute_result execution_count="66"}
    array([[[0.42993897, 0.69747447, 0.50501692, 0.06255893, 0.75110428],
            [0.38412458, 0.42253008, 0.72526108, 0.55720578, 0.01352319],
            [0.87189511, 0.36347656, 0.8511059 , 0.54939943, 0.61046013]],

           [[0.7932152 , 0.34484073, 0.85767667, 0.42652878, 0.69521324],
            [0.73642304, 0.49339807, 0.1555424 , 0.12500141, 0.57821728],
            [0.32849003, 0.08451965, 0.36938592, 0.47934803, 0.4260779 ]],

           [[0.79249832, 0.29956046, 0.25910572, 0.74055872, 0.72708953],
            [0.66064956, 0.61384741, 0.73513558, 0.42477618, 0.71570312],
            [0.35192549, 0.98961731, 0.88115493, 0.65861762, 0.72351593]]])
:::
:::

::: {.cell .code execution_count="67"}
``` {.python}
matrix.T.shape
```

::: {.output .execute_result execution_count="67"}
    (3, 3, 5)
:::
:::

::: {.cell .code execution_count="68"}
``` {.python}
np.random.seed(0)
mat1 = np.random.randint(10, size=(3, 3))
mat2 = np.random.randint(10, size=(3, 2))

mat1.shape, mat2.shape
```

::: {.output .execute_result execution_count="68"}
    ((3, 3), (3, 2))
:::
:::

::: {.cell .code execution_count="69"}
``` {.python}
mat1
```

::: {.output .execute_result execution_count="69"}
    array([[5, 0, 3],
           [3, 7, 9],
           [3, 5, 2]])
:::
:::

::: {.cell .code execution_count="70"}
``` {.python}
mat2
```

::: {.output .execute_result execution_count="70"}
    array([[4, 7],
           [6, 8],
           [8, 1]])
:::
:::

::: {.cell .code execution_count="71"}
``` {.python}
np.dot(mat1, mat2)
```

::: {.output .execute_result execution_count="71"}
    array([[ 44,  38],
           [126,  86],
           [ 58,  63]])
:::
:::

::: {.cell .code execution_count="72"}
``` {.python}
np.random.seed(0)
mat3 = np.random.randint(10, size=(4,3))
mat4 = np.random.randint(10, size=(4,3))
mat3, mat4
```

::: {.output .execute_result execution_count="72"}
    (array([[5, 0, 3],
            [3, 7, 9],
            [3, 5, 2],
            [4, 7, 6]]),
     array([[8, 8, 1],
            [6, 7, 7],
            [8, 1, 5],
            [9, 8, 9]]))
:::
:::

::: {.cell .code execution_count="73"}
``` {.python}
np.dot(mat3, mat4)
```

::: {.output .error ename="ValueError" evalue="shapes (4,3) and (4,3) not aligned: 3 (dim 1) != 4 (dim 0)"}
    ---------------------------------------------------------------------------
    ValueError                                Traceback (most recent call last)
    /home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb Cell 114' in <cell line: 1>()
    ----> <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000114?line=0'>1</a> np.dot(mat3, mat4)

    File <__array_function__ internals>:180, in dot(*args, **kwargs)

    ValueError: shapes (4,3) and (4,3) not aligned: 3 (dim 1) != 4 (dim 0)
:::
:::

::: {.cell .code execution_count="74"}
``` {.python}
mat3.T.shape
```

::: {.output .execute_result execution_count="74"}
    (3, 4)
:::
:::

::: {.cell .code execution_count="75"}
``` {.python}
# Dot product
np.dot(mat3.T, mat4)
```

::: {.output .execute_result execution_count="75"}
    array([[118,  96,  77],
           [145, 110, 137],
           [148, 137, 130]])
:::
:::

::: {.cell .code execution_count="76"}
``` {.python}
# Element-wise multiplication, also known as Hademard product
mat3 * mat4
```

::: {.output .execute_result execution_count="76"}
    array([[40,  0,  3],
           [18, 49, 63],
           [24,  5, 10],
           [36, 56, 54]])
:::
:::

::: {.cell .markdown}
## Dot product practical example, nut butter sales
:::

::: {.cell .code execution_count="77"}
``` {.python}
np.random.seed(0)
sales_amounts = np.random.randint(20, size=(5, 3))
sales_amounts
```

::: {.output .execute_result execution_count="77"}
    array([[12, 15,  0],
           [ 3,  3,  7],
           [ 9, 19, 18],
           [ 4,  6, 12],
           [ 1,  6,  7]])
:::
:::

::: {.cell .code execution_count="81"}
``` {.python}
weekly_sales = pd.DataFrame(sales_amounts,
                            index=["Mon", "Tues", "Wed", "Thurs", "Fri"],
                            columns=["Almond butter", "Peanut butter", "Cashew butter"])
weekly_sales
```

::: {.output .execute_result execution_count="81"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Almond butter</th>
      <th>Peanut butter</th>
      <th>Cashew butter</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Mon</th>
      <td>12</td>
      <td>15</td>
      <td>0</td>
    </tr>
    <tr>
      <th>Tues</th>
      <td>3</td>
      <td>3</td>
      <td>7</td>
    </tr>
    <tr>
      <th>Wed</th>
      <td>9</td>
      <td>19</td>
      <td>18</td>
    </tr>
    <tr>
      <th>Thurs</th>
      <td>4</td>
      <td>6</td>
      <td>12</td>
    </tr>
    <tr>
      <th>Fri</th>
      <td>1</td>
      <td>6</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="82"}
``` {.python}
prices = np.array([10, 8, 12])
prices
```

::: {.output .execute_result execution_count="82"}
    array([10,  8, 12])
:::
:::

::: {.cell .code execution_count="83"}
``` {.python}
butter_prices = pd.DataFrame(prices.reshape(1,3),
                            index=["Price"],
                            columns=["Almond butter", "Peanut butter", "Cashew butter"])
butter_prices, butter_prices.shape
```

::: {.output .execute_result execution_count="83"}
    (       Almond butter  Peanut butter  Cashew butter
     Price             10              8             12,
     (1, 3))
:::
:::

::: {.cell .code execution_count="84"}
``` {.python}
weekly_sales
```

::: {.output .execute_result execution_count="84"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Almond butter</th>
      <th>Peanut butter</th>
      <th>Cashew butter</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Mon</th>
      <td>12</td>
      <td>15</td>
      <td>0</td>
    </tr>
    <tr>
      <th>Tues</th>
      <td>3</td>
      <td>3</td>
      <td>7</td>
    </tr>
    <tr>
      <th>Wed</th>
      <td>9</td>
      <td>19</td>
      <td>18</td>
    </tr>
    <tr>
      <th>Thurs</th>
      <td>4</td>
      <td>6</td>
      <td>12</td>
    </tr>
    <tr>
      <th>Fri</th>
      <td>1</td>
      <td>6</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="85"}
``` {.python}
# Find the total amount of sales for a whole day
tottal_sales = prices.dot(sales_amounts)
tottal_sales
```

::: {.output .error ename="ValueError" evalue="shapes (3,) and (5,3) not aligned: 3 (dim 0) != 5 (dim 0)"}
    ---------------------------------------------------------------------------
    ValueError                                Traceback (most recent call last)
    /home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb Cell 32' in <cell line: 2>()
          <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000031?line=0'>1</a> # Find the total amount of sales for a whole day
    ----> <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000031?line=1'>2</a> tottal_sales = prices.dot(sales_amounts)
          <a href='vscode-notebook-cell:/home/anis/Documents/zero-to-mastery-ml/Exercise/Numpy/basic-numpy.ipynb#ch0000031?line=2'>3</a> tottal_sales

    ValueError: shapes (3,) and (5,3) not aligned: 3 (dim 0) != 5 (dim 0)
:::
:::

::: {.cell .code execution_count="88"}
``` {.python}
prices, prices.shape
```

::: {.output .execute_result execution_count="88"}
    (array([10,  8, 12]), (3,))
:::
:::

::: {.cell .code execution_count="87"}
``` {.python}
sales_amounts.T.shape
```

::: {.output .execute_result execution_count="87"}
    (3, 5)
:::
:::

::: {.cell .code execution_count="89"}
``` {.python}
# zto make the middle numbers the same, we can tranpose
tottal_sales = prices.dot(sales_amounts.T)
tottal_sales
```

::: {.output .execute_result execution_count="89"}
    array([240, 138, 458, 232, 142])
:::
:::

::: {.cell .code execution_count="90"}
``` {.python}
butter_prices.shape, weekly_sales.shape
```

::: {.output .execute_result execution_count="90"}
    ((1, 3), (5, 3))
:::
:::

::: {.cell .code execution_count="91"}
``` {.python}
daily_sales = butter_prices.dot(weekly_sales.T)
daily_sales
```

::: {.output .execute_result execution_count="91"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Mon</th>
      <th>Tues</th>
      <th>Wed</th>
      <th>Thurs</th>
      <th>Fri</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Price</th>
      <td>240</td>
      <td>138</td>
      <td>458</td>
      <td>232</td>
      <td>142</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="92"}
``` {.python}
# Need to transpose again
weekly_sales["Total"] = daily_sales.T
weekly_sales
```

::: {.output .execute_result execution_count="92"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Almond butter</th>
      <th>Peanut butter</th>
      <th>Cashew butter</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Mon</th>
      <td>12</td>
      <td>15</td>
      <td>0</td>
      <td>240</td>
    </tr>
    <tr>
      <th>Tues</th>
      <td>3</td>
      <td>3</td>
      <td>7</td>
      <td>138</td>
    </tr>
    <tr>
      <th>Wed</th>
      <td>9</td>
      <td>19</td>
      <td>18</td>
      <td>458</td>
    </tr>
    <tr>
      <th>Thurs</th>
      <td>4</td>
      <td>6</td>
      <td>12</td>
      <td>232</td>
    </tr>
    <tr>
      <th>Fri</th>
      <td>1</td>
      <td>6</td>
      <td>7</td>
      <td>142</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .markdown}
## Comparison operators
:::

::: {.cell .code execution_count="93"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="93"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="94"}
``` {.python}
a2
```

::: {.output .execute_result execution_count="94"}
    array([[1. , 3. , 3.3],
           [2. , 5. , 6.5]])
:::
:::

::: {.cell .code execution_count="95"}
``` {.python}
a1 > a2
```

::: {.output .execute_result execution_count="95"}
    array([[False, False, False],
           [False, False, False]])
:::
:::

::: {.cell .code execution_count="96"}
``` {.python}
a1 >= a2
```

::: {.output .execute_result execution_count="96"}
    array([[ True, False, False],
           [False, False, False]])
:::
:::

::: {.cell .code execution_count="97"}
``` {.python}
a1 > 5
```

::: {.output .execute_result execution_count="97"}
    array([False, False, False])
:::
:::

::: {.cell .code execution_count="98"}
``` {.python}
a1 == a1
```

::: {.output .execute_result execution_count="98"}
    array([ True,  True,  True])
:::
:::

::: {.cell .code execution_count="99"}
``` {.python}
a1 == a2
```

::: {.output .execute_result execution_count="99"}
    array([[ True, False, False],
           [False, False, False]])
:::
:::

::: {.cell .code execution_count="100"}
``` {.python}
a1.sum() < a2.sum()
```

::: {.output .execute_result execution_count="100"}
    True
:::
:::

::: {.cell .markdown}
## 5. Sorting arrays {#5-sorting-arrays}
:::

::: {.cell .code execution_count="105"}
``` {.python}
random_array
```

::: {.output .execute_result execution_count="105"}
    array([[8, 1, 3],
           [3, 3, 7],
           [0, 1, 9],
           [9, 0, 4],
           [7, 3, 2]])
:::
:::

::: {.cell .code execution_count="106"}
``` {.python}
np.sort(random_array)
```

::: {.output .execute_result execution_count="106"}
    array([[1, 3, 8],
           [3, 3, 7],
           [0, 1, 9],
           [0, 4, 9],
           [2, 3, 7]])
:::
:::

::: {.cell .code execution_count="110"}
``` {.python}
np.argsort(random_array)
```

::: {.output .execute_result execution_count="110"}
    array([[1, 2, 0],
           [0, 1, 2],
           [0, 1, 2],
           [1, 2, 0],
           [2, 1, 0]])
:::
:::

::: {.cell .code execution_count="111"}
``` {.python}
a1
```

::: {.output .execute_result execution_count="111"}
    array([1, 2, 3])
:::
:::

::: {.cell .code execution_count="112"}
``` {.python}
# Return the indices that would sort an array
np.argsort(a1)
```

::: {.output .execute_result execution_count="112"}
    array([0, 1, 2])
:::
:::

::: {.cell .code execution_count="113"}
``` {.python}
# No axis
np.argmin(a1)
```

::: {.output .execute_result execution_count="113"}
    0
:::
:::

::: {.cell .code execution_count="118"}
``` {.python}
random_array
```

::: {.output .execute_result execution_count="118"}
    array([[8, 1, 3],
           [3, 3, 7],
           [0, 1, 9],
           [9, 0, 4],
           [7, 3, 2]])
:::
:::

::: {.cell .code execution_count="115"}
``` {.python}
np.argmax(a1)
```

::: {.output .execute_result execution_count="115"}
    2
:::
:::

::: {.cell .code execution_count="116"}
``` {.python}
# Down the vertical
np.argmax(random_array, axis=1)
```

::: {.output .execute_result execution_count="116"}
    array([0, 2, 2, 0, 0])
:::
:::

::: {.cell .code execution_count="117"}
``` {.python}
# Across the horizontal
np.argmin(random_array,axis=0)
```

::: {.output .execute_result execution_count="117"}
    array([2, 3, 4])
:::
:::

::: {.cell .markdown}
## 6. Use case {#6-use-case}
:::

::: {.cell .code execution_count="120"}
``` {.python}
from matplotlib.image import imread

panda = imread("index.jpg")
print(type(panda))
```

::: {.output .stream .stdout}
    <class 'numpy.ndarray'>
:::
:::

::: {.cell .code execution_count="121"}
``` {.python}
panda.shape
```

::: {.output .execute_result execution_count="121"}
    (183, 275, 3)
:::
:::

::: {.cell .code execution_count="122"}
``` {.python}
panda
```

::: {.output .execute_result execution_count="122"}
    array([[[ 82,  92, 101],
            [ 79,  89,  98],
            [ 76,  85,  92],
            ...,
            [ 50,  51,  46],
            [ 39,  44,  37],
            [ 39,  44,  37]],

           [[ 82,  92, 101],
            [ 80,  90,  99],
            [ 77,  86,  93],
            ...,
            [ 63,  59,  56],
            [ 43,  42,  37],
            [ 28,  27,  22]],

           [[ 83,  93, 102],
            [ 81,  91, 100],
            [ 78,  87,  94],
            ...,
            [ 95,  81,  81],
            [ 72,  56,  57],
            [ 49,  33,  34]],

           ...,

           [[136, 127, 122],
            [134, 125, 120],
            [131, 121, 119],
            ...,
            [ 27,  26,  32],
            [ 26,  27,  32],
            [ 27,  28,  33]],

           [[131, 122, 117],
            [131, 122, 117],
            [130, 120, 118],
            ...,
            [ 31,  30,  36],
            [ 31,  32,  37],
            [ 31,  32,  37]],

           [[127, 118, 113],
            [128, 119, 114],
            [129, 119, 117],
            ...,
            [ 34,  33,  39],
            [ 34,  35,  40],
            [ 34,  35,  40]]], dtype=uint8)
:::
:::
