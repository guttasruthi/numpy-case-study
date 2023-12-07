```python
import numpy as np
```


```python
p = (r'C:\Users\HP\Desktop\Numpy\train_extended.csv')
```


```python
x = np.genfromtxt(p,delimiter=',',skip_header = True)
x
```




    array([[ 1.575     ,  1.225     ,  0.375     , ...,  6.3219385 ,
             9.63883   , 10.        ],
           [ 1.2375    ,  1.        ,  0.375     , ...,  3.798833  ,
             7.654365  , 19.        ],
           [ 1.45      ,  1.1625    ,  0.4125    , ...,  7.01650125,
             7.257472  , 11.        ],
           ...,
           [ 1.125     ,  0.9125    ,  0.2875    , ...,  1.984465  ,
             3.118445  ,  7.        ],
           [ 1.625     ,  1.275     ,  0.4125    , ...,  7.86698625,
            10.489315  , 11.        ],
           [ 1.5875    ,  1.25      ,  0.3875    , ...,  7.38504475,
             8.788345  , 11.        ]])



## 1) What is the shape of array?


```python
a = np.shape(x)
a


```




    (200000, 8)



## 2)What is the maximum and minimum length?


```python
min_length = np.min(x[:,0])
max_length = np.max(x[:,0])
print(f'the minimun length is:{min_length}')
print(f'the maximum length is:{max_length}')

```

    the minimun length is:0.0
    the maximum length is:7.58349125
    

## 3) What is the average weight?


```python
weight = x[:,3]
```


```python
avg_weight = np.mean(weight)
print(f'the average weight is:{avg_weight}')


```

    the average weight is:23.123436312982403
    

## 4)which column has highest average.?


```python
length = x[:,0]
diameter = x[:,1]
height = x[:,2]
weight = x[:,3]
shucked_weight = x[:,4]
viscera_weight = x[:,5]
shell_weight = x[:,6]
age = x[:,7]
avg_length = np.mean(length)
avg_diameter = np.mean(diameter)
avg_height = np.mean(height)
avg_weight = np.mean(weight)
avg_shucked_weight = np.mean(shucked_weight)
avg_viscera_weight = np.mean(viscera_weight)
avg_shell_weight = np.mean(shell_weight)
avg_age = np.mean(age)
print(f'the avg length is:{avg_length}')
print(f'the avg diameter is:{avg_diameter}')
print(f'the avg height is:{avg_height}')
print(f'the avg weight is:{avg_weight}')
print(f'the avg shucked_weight is:{avg_shucked_weight}')
print(f'the avg viscera_weight is:{avg_viscera_weight}')
print(f'the avg shell_weight is:{avg_shell_weight}')
print(f'the avg age is:{avg_age}')



```

    the avg length is:1.3124480799562501
    the avg diameter is:1.020320357165
    the avg height is:0.34602787104999994
    the avg weight is:23.123436312982403
    the avg shucked_weight is:9.989370248049001
    the avg viscera_weight is:4.993180956748749
    the avg shell_weight is:6.634229147607001
    the avg age is:9.950615
    

## 8)what is the total  Shell Weight?




```python
shell_weight = x[:,3]
```


```python
total_shell = np.sum(shell_weight)
print(f'the total weight is:{total_shell}')
```

    the total weight is:4624687.262596481
    

## 10)What is the average height of persons whose age is between 14 and 19?


```python
height= 2
age = 7
a = x[(x[:, age] >= 14) & (x[:, age] <= 19)]
z = np.mean(a[:,height])
print(z)

```

    0.41489902051107985
    

## 9)what is the count of rows where height is >0.4 and weight >55. and age<11 and Viscera Weight<4


```python
height = 2
weight = 3
age = 7
viscera = 5
aa = x[(x[:,age] < 11) & (x[:,viscera] < 4) & (x[:,height]>0.4) & (x[:,weight]>55)]
zz = aa.shape[0]
print(zz)
        


```

    0
    

## 7) what is the count of rows where height is >0.4 and weight >55.



```python
height = 2
weight = 3
h = x[(x[:,height] > 0.4) & (x[:,weight] > 55)]
w = h.shape[0]
print(w)
```

    1390
    

## 6)how many rows in the data where height is >0.4.



```python
height = 2
data = (x[(x[:,height] > 0.4)])
rows = data.shape[0]
print(rows)
```

    55336
    


```python

```


```python


```


```python

```
