# JupyterLab
 web-based user interface for Project Jupyter.


jpuitar lab has its own terminal and work area is divided into **cells**

each cell has excuation order 

You can arrange multiple documents and activities side by side in the work area using tabs and splitters

you can use it on nearlly all kinds of files

jupitar has 2 mods 

1- command mode

2- edit mode 



you can change cell format to code or mark down using keyboard shortcuts

 enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components 


# NumPy

 all data must be of th esame type in numpy array  , it get converted automatically by numpy to be all of the same type 
 
a- arr.ndim   # number of diminsiion

b- np.arr=( [1,2] , ndmin = num  )      # min num of diminsions

d- np.arange(50)    # same as range (from 0-49)

d- dtype= ''
 Python data analysis package

numpy array are ndarray  (number of diminsional array)

## numpy array
   numpy array is faser than list or swt or tuple 

 In a NumPy array, the number of dimensions is called the **rank**, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.
 
 1D array : reslut of 0 D elemnts ex ( [ 0,1,2  ] )   #  3 elemnt  every elemnt is called 0 D  array 
  
 2D array: result of 1  D elemnt ex: ( [  0,1,2],[3,4,5  ] )   # 2 elemnts every elemnt is 1 D array   **matrix**     **numpy.mat()**
  
 3D array : result of 2 D elemnts  ex : ( [  [[0,1,2],[3,4,5]] ,  [[0,1,2],[3,4,5]]  ] )    2 elemnts every elemnt is 2D array
 
 
 
 
 ## to check how many dimenisions in numpy array   (ndim)
 
 number of diminsion
 
```
import numpy as np

a = np.array(42) 
b = np.array([1, 2, 3, 4, 5])
c = np.array([[1, 2, 3], [4, 5, 6]])
d = np.array([[[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]]])

print(a.ndim)   # 0
print(b.ndim)   # 1
print(c.ndim)   # 2
print(d.ndim)   # 3
```

### Creating A NumPy Array

(ndmin: specifiy how many D is your array )

We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. 


There are a variety of methods that you can use to create NumPy arrays. To start with, you can create an array where every element is zero. 
**It’s useful to create an array with all zero elements in cases when you need an array of fixed size, but don’t have any values for it yet.**
```
 arr=np.array([1,2,3,4])  
arr = np.array([1, 2, 3, 4], ndmin=5)  # ndmin  is optional
```



## Indexing NumPy Arrays

. We can use array indexing to select individual elements, groups of elements, or entire rows and columns

 NumPy is zero-indexed, meaning that the index of the first row is 0, and the index of the first column is 0
 
 
 ```
 arr = np.array([1, 2, 3, 4])

print(arr[2] + arr[3])     # 3 + 4 = 7 
 ```
 
 
## access to  array items
```

import numpy as np

arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])

print('2nd element on 1st row: ', arr[0, 1]) == arr[0][1]   # 2       # Access the element on the first row, second column

print('5th element on 2nd row: ', arr[1, 4])   # 10      



arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

print(arr[0, 1, 2])             # 6                        # Access the third element of the second array of the first array:



arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])

print('Last element from 2nd dim: ', arr[1, -1])          # 10 


```



## Slicing arrays

We pass slice instead of index like this: `[start:end].`


We can also define the step, like this: `[start:end:step].`


If we don't pass `start` its considered 0


If we don't pass `end` its considered length of array in that dimension


If we don't pass `step` its considered 1

 
  **The result includes the start index, but excludes the end index.**

 we can do it using a colon (:). A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. This is also known as a slice.
 
 ```
 import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[4:])     # [ 5 , 6 , 7]     # THE END WAS nos specified so it will be in the result 
print(arr[4: -1] )  # [5 , 6]    
 ``` 
 
 ##  slicing 2 d  array  ######## 
 
 arr [slice array  ,  slice ele in array ]
 
 print(arr[0:2, 2]) 
 arr[0:2]    in 2d arrray means slice the first 2 array (1 D) array from the 2 D array 
        2    means from each 1 D array slice the secound element 
```
arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])    

print(arr[1, 1:4])      # [7 , 8 ,9 ]      # From the second element, slice elements from index 1 to index 4 (not included):



arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])    

print(arr[0:2, 2])           #   [3 8]                        # From both elements, return index 2:


arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]]) 

print(arr[0:2, 1:4])     #    [[2 3 4] [7 8 9]]              # From both elements, slice index 1 to index 4 (not included), this will return a 2-D array:
```


## Numpy datatypes   ( dtype = '' )

NumPy has several different data types, which mostly map to Python data types, like float, and str

`float` — numeric floating point data.  (f)

`int` — integer data.  (i)

`string` — character data.  ( s )

`datetime`  -    ( m )

`object` — Python objects.   ( o )

```
import numpy as np

arr = np.array([1, 2, 3, 4], dtype='S')

print(arr)                   # ['1' ,'2' ,'3' ,'4']

print(arr.dtype)          # S
```

## Converting Data Types   (arr.astype(''))

 can use the `numpy.ndarray.astype` method to convert an array to a different type. 

```
import numpy as np

arr = np.array([1.1, 2.1, 3.1])

newarr = arr.astype('i')

print(newarr)
print(newarr.dtype)

```

## NumPy Array Copy  vs view
The main difference between a copy and a view of an array is that the copy is a new array, and the view is just a view of the original array

Every NumPy array has the attribute `base` that returns `None` if the array owns the data.

Otherwise, the base  attribute refers to the `original object`.

```
Make a copy, change the original array, and display both arrays:

import numpy as np

arr = np.array([1, 2, 3, 4, 5])
x = arr.copy()
arr[0] = 42

print(arr)
print(x)
```


## NumPy Array Shape  ( shape )

The shape of an array is the number of elements in each dimension.

 `shape` that returns a tuple with each index having the number of corresponding elements.
 
 
 ```
 import numpy as np

arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

print(arr.shape)      # (2,4)  tuple that states it has 2 items each one has 4 elemnts



# Create an array with 5 dimensions using ndmin using a vector with values 1,2,3,4 and verify that last dimension has value 4:

arr = np.array([1, 2, 3, 4], ndmin=5)

print(arr)                                 ## [[[[[1 2 3 4]]]]]
print('shape of array :', arr.shape)       ## shape of array : (1, 1, 1, 1, 4)

 ```
 
 
##  Reshaping arrays

Reshaping means changing the shape of an array.

```


import numpy as np


## Reshape From 1-D to 2-D

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

newarr = arr.reshape(4, 3)        # conver it to array with 4 elem and every ele has 3 elemnts

print(newarr)

# output 
[[ 1  2  3]
 [ 4  5  6]
 [ 7  8  9]
 [10 11 12]]
 
 ## Reshape From 1-D to 3-D
 

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

newarr = arr.reshape(2, 3, 2)   # The outermost dimension will have 2 arrays that contains 3 arrays, each with 2 elements:

print(newarr)

# output 

[[[ 1  2]
  [ 3  4]
  [ 5  6]]

 [[ 7  8]
  [ 9 10]
  [11 12]]]


```
### note

The view does not own the data and any changes made to the view will affect the original array, and any changes made to the original array will affect the view.

The example above returns the original array, so it is a view.


## Unknown Dimension
You are allowed to have one "unknown" dimension. Meaning that you do not have to specify an exact number for one of the dimensions in the reshape method.

Pass -1 as the value, and NumPy will calculate this number for you.
```
Example
Convert 1D array with 8 elements to 3D array with 2x2 elements:

import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])

newarr = arr.reshape(2, 2, -1)

print(newarr)
```

## Flattening the arrays  `reshape(-1)`   or  `eval()`

Flattening array means converting a multidimensional array into a 1D array.


#  NumPy Array Iterating

1- If we iterate on a n-D array it will go through n-1th dimension one by one. (using normal loop)

 2- iterate using `np.nditer(arr, flags=['buffered'], op_dtypes=['S'])`   
 

3- Enumerated Iteration Using `ndenumerate()`
## Iterating Arrays Using `nditer()`

```
import numpy as np

arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

for x in np.nditer(arr):
  print(x)

# output 
1
2
3
4
5
6
7
8
```

## Iterating Array With Different Data Types   (op_dtypes='')

`op_dtypes` argument and pass it the expected datatype to change the datatype of elements while iterating.

NumPy does not change the data type of the element in-place (where the element is in array) so it needs some other space to perform this action, that extra space is called **buffer,** and in order to enable it in `nditer()` we pass `flags=['buffered']`.

```
import numpy as np

arr = np.array([1, 2, 3])

for x in np.nditer(arr, flags=['buffered'], op_dtypes=['S']):
  print(x)         # result all x will be printed as strings 
```

## numerated Iteration Using ndenumerate()
Enumeration means mentioning sequence number of somethings one by one.

Sometimes we require corresponding index of the element while iterating, the ndenumerate() method can be used for those usecases.


```
import numpy as np

arr = np.array([1, 2, 3])

for idx, x in np.ndenumerate(arr):
  print(idx, x)
  
  #output 
  
(0,) 1
(1,) 2
(2,) 3

### iterate through 2D array

import numpy as np

arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])

for idx, x in np.ndenumerate(arr):
  print(idx, x)
 
   ```
   ```
    (0, 0) 1
 (0, 1) 2
 (0, 2) 3
 (0, 3) 4
 (1, 0) 5
 (1, 1) 6
 (1, 2) 7
 (1, 3) 8 
   ```


## Joining NumPy Arrays




## Using NumPy To Read In Files

It’s possible to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function.
 ## Assigning Values To NumPy Arrays


 use indexing to assign values to certain elements in arrays. We can do this by assigning directly to the indexed value

 `wines[1,5] = 10`


 **To overwrite an entire column, we can do this:**

`wines[:,10] = 50`

The above code overwrites all the values in the eleventh column with 50.

** NumPy is a package for working with multidimensional arrays**
+ 1-Dimensional NumPy Arrays


+ N-Dimensional NumPy Arrays






 ## NumPy Array Operations

NumPy makes it simple to perform mathematical operations on arrays. This is one of the primary advantages of NumPy, and makes it quite easy to do computations.

**+ Single Array Math**

If you do any of the basic mathematical operations (/, *, -, +, ^) with an array and a value, it will apply the operation to each of the elements in the array.

**+ Multiple Array Math**

it’s also possible to do mathematical operations between arrays


## Broadcasting

try to match up elements. Essentially, broadcasting involves a few steps:

The last dimension of each array is compared.

If the dimension lengths are equal, or one of the dimensions is of length 1, then we keep going.

If the dimension lengths aren’t equal, and none of the dimensions have length 1, then there’s an error.

Continue checking dimensions until the shortest array is out of dimensions.


## NumPy Array Methods


NumPy also has several methods that you can use for more complex calculations on arrays. An example of this is the `numpy.ndarray.sum method` This finds the sum of all the elements in an array by default

There are several other methods that behave like the sum method, including:

`numpy.ndarray.mean` — finds the mean of an array.
`numpy.ndarray.std` — finds the standard deviation of an array.
`numpy.ndarray.min` — finds the minimum value in an array.
`numpy.ndarray.max` — finds the maximum value in an array.


## NumPy Array Comparisons


NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations like <, >, >=, <=, and ==.

## Subsetting
 select only certain rows or columns in the NumPy array

 ## Reshaping NumPy Arrays

 change the shape of arrays while still preserving all of their elements.

 We can use the `numpy.ravel` function to turn an array into a one-dimensional representation

 ## Combining NumPy Arrays
 it’s very common to combine multiple arrays into a single unified array. We can use `numpy.vstack` 


## [Free NumPy Cheat Sheet](https://s3.amazonaws.com/dq-blog-files/numpy-cheat-sheet.pdf)
