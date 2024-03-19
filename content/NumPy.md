---
title: NumPy
draft: false
tags:
---
## Introduction 
- NumPy stands for numerical [[Python]] and it turns data into numbers that the computer can analyze to find patterns 
- We use NumPy because it's fast and it's optimized using C in the background 
## Data Types and Attributes 
`ndarray`: n-dimensional array 
- `.ndim`: number of dimensions 
- `.dtype`: datatype 
- `.shape`: tells you the shape (row, column, beyond)
- `.size`: how many elements in the array 
```python 
import numpy as np
# 1 dimensional array 
a1 = np.array([1,2,3])
# 2 dimensional array
a2 = np.array([[1,2,3],
			   [4,5,6]])
# 3 dimensional array 
a3 = np.array([[[1,2,3],
			   [4,5,6], 
			   [7,8,9]],
			   [[10,11,12],
			   [13,14,15],
			   [16,17,18]]])
```
## Creating arrays 
- `shift + tab` in jupyter notebook will show you the info from the documentation 
- `np.ones(shape)`: array in the shape specified filled with ones 
- `np.zeros(shape)`: array in the shape specified filled with zeros
- `np.arange(start,stop,step)`
- `np.random.randint(low,high,shape)`
- `np.random.random(shape)`
### Random Seed 
- Note: random numbers are **pseudo-random** 
- `np.random.seed(seed=num)`: allows you to randomly generate things in a reproducible way 
## Viewing arrays and matrices 
- `np.unique(array)`: returns the unique values of the array 
- You can index and slice the arrays like you would normally in Python lists 
- Tip: the last number in the shape is usually the inner-most array size 
## Manipulating & comparing arrays 
- `arr1 + arr2` or `np.add(arr1, arr2)`: adds the two arrays together 
- Most standard arithmetic is compatible with arrays as well 
- Important note: Not all shapes are compatible for arithmetic though so keep that in mind!  
	- The term for shape compatibility is ==broadcasting== 
- Dimensions are compatible if: 
	- they are equal to each other 
	- one of the numbers is 1
### Aggregation 
- Aggregation is performing the same operation on a number of objects 
- `sum(arr1)` vs `np.sum(arr1)`
	- Use the Python operation on Python datatypes and the NumPy operations on NumPy operations 
- `np.mean()`
- `np.max()`
- `np.min()`
- `np.std()`: standard deviation 
	- ==Standard deviation==: measure of how spread out a group of numbers is from the mean (square root of the variance)
- `np.var()`: variance 
	- ==Variance==: measure of the average degree to which each number is different to the mean (ie: Higher variance = wider range of numbers)
## Reshaping & transposing arrays 
- `.reshape(shape)`: reshapes the array to the desired shape 
- `.T`: transposes the array meaning that it swaps the axises 
## Dot product 
- `np.dot(arr1, arr2)`: dot product aka matrix multiplication
	- Requirement: the inside numbers of the shape have to be equal 
	- Result: produces a matrix that's the shape of the outside numbers 
## Sorting arrays 
- `np.sort(arr)`:  sorts each row 
- `np.argsort(arr)`: tells you the index the value will be when sorted
- `np.argmin(arr,axis)`, `np.argmax(arr,axis)`: finds the minimum or maximum value in the specified axis. Axises are "flipped":
	- `axis=0` looks at the columns 
	- `axis=1` looks at the rows 
## Practical example: turn an image into NumPy array 
```python 
from matplotlib.image import imread
# turn panda image into an array 
panda = imread("file-name.png")
```
## Other methods & functions 
- `np.linespace()` returns evenly spaced numbers over a specified interval
- `np.random.radn(size)` creates a data set that has a normal distribution 