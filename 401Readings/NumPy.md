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

 Python data analysis package


## numpy array

 In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.

### Creating A NumPy Array

We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. 


There are a variety of methods that you can use to create NumPy arrays. To start with, you can create an array where every element is zero. 
**It’s useful to create an array with all zero elements in cases when you need an array of fixed size, but don’t have any values for it yet.**


## Using NumPy To Read In Files

It’s possible to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function.



## Indexing NumPy Arrays

. We can use array indexing to select individual elements, groups of elements, or entire rows and columns

 NumPy is zero-indexed, meaning that the index of the first row is 0, and the index of the first column is 0




 ## Slicing NumPy Arrays

 we can do it using a colon (:). A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. This is also known as a slice.


 ## Assigning Values To NumPy Arrays


 use indexing to assign values to certain elements in arrays. We can do this by assigning directly to the indexed value

 `wines[1,5] = 10`


 **To overwrite an entire column, we can do this:**

`wines[:,10] = 50`

The above code overwrites all the values in the eleventh column with 50.

** NumPy is a package for working with multidimensional arrays**
+ 1-Dimensional NumPy Arrays


+ N-Dimensional NumPy Arrays



## Numpy datatypes

NumPy has several different data types, which mostly map to Python data types, like float, and str

`float` — numeric floating point data.

`int` — integer data.

`string` — character data.

`object` — Python objects.


## Converting Data Types

 can use the `numpy.ndarray.astype` method to convert an array to a different type. 



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
