**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library

# Definition
NumPy is a Python library that provides a simple yet powerful data structure: the **n-dimensional array**. Written in C, numpy is more powerfull and faster than python's lists. Conditions and loops run 2-8x faster, overall 30% faster for plain Python code

# Code notes
## Creating
Create numpy's ndarray:
```python
import numpy as np

# new numpy array
np_array = np.array([[1, 2, 3], [4, 5, 6]])

# new numpy array from python's list
py_list = [1, 2, 3, 4, 5]
np_array = np.array(py_list)
```

## Having informations
Print shape of an array:
```python
np.array.shape
```

## Slicing
`ndarray[:X]` where $X$ is integer, slice all elements before row $X$.
```python
np_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

np_array[:2]
# Print is : array([[1, 2, 3],
#					[4, 5, 6]])
```
`ndarray[:, :X]` where $X$ is integer, slice all data from all rows, but just only on $X$ column.
```python
np_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

np_array[:, :2]
# Print is : array([[1],
#					[4],
#					[7]])
```
`ndarray[V:W, X:Y]` where $V$, $W$, $X$, $Y$ are integers, slice index $X$ to index $Y$ (not included), this will return a 2-D array.
```python
np_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

np_array[1:3, 1:3]
# Print is : array([[5, 6],
#					[8, 9]])
```

## Integer array indexing
`my_np_array[[A, B, C], [X, Y, Z]]` keep data on $A$, $B$, and $C$ rows, and $X$, $Y$, $Z$, columns.
```python
my_np_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])

my_np_array[[0, 1, 2], [0, 1, 2]]
# Print is : array([1, 5, 9])
```

## Boolean masking
Print boolean response, in this exemple print true if number is even and false if it's odd.
```python
my_np_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])

bool_mask = my_np_array%2==0

bool_mask
```

## Numerical operations
Numpy's arrays can compute numerical operations on ndarray.
```python
np_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Multiplying
new_np_array = np_array * 2
# or
np.multiply(arr1, arr2)

# Squared
new_np_array = np_array ** 2

# Dividing
new_np_array = np_array / 2

# Sum
np_array1 + np_array2
```
More on [Math numpy documentation](https://numpy.org/doc/stable/reference/routines.math.html).

# Using with [[Cython]]
Numpy can be use in Cython for more fast computing. `@boundscheck` and `@wraparound` are checks for Cython's arrays. `@boundscheck` deactivate bounds checking, `@wraparound` deactivate negative indexing.
```cython
import numpy as np

from cython import boundscheck, wraparound

x = np.random.randn(50000)
y = np.random.randn(50000)

@boundscheck(False)
@wraparound(False)
def do_some_op_no_bounds(double[::1] x, double[::1] y):
	cdef int n_x = x.size
	cdef int n_y = y.size
	if n_x!=n_y:
		return "Invalid Array input! Both array should be of same size"
	cdef double[::1] z = np.zeros(n_x)
	cdef int i
	for i in range(0, n_x):
		z[i] = x[i] + y[i] + i
	return z
```
