**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library

# Definition
[Dask](https://www.dask.org) is a scalable library for parallel computing using Python. It can scale easily from a single to a multiple cluster. It contains specialized task scheduling components for efficient computation of data. It also provides collections (data structures) for parallel and [[Distributed System]] computing of resources. **Documenation** can be found [here](https://docs.dask.org/en/stable/).

# Use cases
- Sometimes we encounter data that does not fit into the memory, Dask can break the data into manageable chunks and process them individually.
- It's desgined to work with existing Python libraries like Numpy, Pandas, and so on so, not much code needs to be changes.
- It can parallelize our existing code to make use of multiple cores on single machine.

# Limitations
- In a distributed setting, the workers have the same limitations of Python processes.
- Assigning of tasks to workers may not always be optimal.
- It make the assumption that your data and functions are both serializable.

# Blocked algorithms
Dask essentialy breaks large datasets into smaller/mangeable chunks or blocks of memory. Blocked algorithms are designed to work on these chunks / blocks of memory. The basic idea is to perform large computations and then aggregating the final result from these smaller ones. It consists of multiple [[Numpy]] array arranged in a grid for efficient computation.

# Installation
With conda:
```shell
conda install dask
```
With pip (only core parts of dask):
```shell
pip install dask
```
With pip (with all parts):
```shell
pip install "dask[complete]"
```
# Code notes
## Basics
- Equivalent of [[Numpy]] `ndarray` (but with larger memory) is just `array`, with capability of decomposing it in chunks of data (**#ex1**). Dask does lazy evaluation. We need to call `da.compute()` to execute statements.
- `ndarray` can be converted to Dask `array` (**#ex2**).
- Dask can transform two DataFrames in one with `da.add()` method (**ex3**).
`DataFrame.compute()` turns a lazy Dask collection into its in-memory equivalent. For example a Dask array turns into a NumPy array and a Dask dataframe turns into a Pandas dataframe. The entire dataset must fit into memory before calling this operation.
```python
import dask.array as da

# ex1
dask_arr1 = da.random.random(10, chunks=3)
dask_arr1.compute()

# ex2
arr1 = np.random.random(10)
dask_arr2 = da.from_array(arr1, chunks=4)

#ex3
da_arr3 = da.add(dask_arr1, dask_arr2)
```

## Parallel computing
 >`Dask.delayed` or `@delayed` decorator allows us to parallelize custom code which otherwise cannot be parallelized using dask arrays. If the function is parallelizable, then the [[Decorator]] function is parallelized internally using task graphs in Dask. It also causes the function to be lazily evaluated. Task graph can be visualizated by the visualize function.

In this example `@delayed` decorator enable function to be parallelized. `visualize()` print task graph.
```python
from dask import delayed, compute


@delayed
def do_op1(x, y, z):
	return x + y - (2 - z)


@delayed
def do_op2(a, b):
	return a * b + 3


@delayed
def do_op3(p):
	return p*p*p


final_result = []
for i in range(0, x.size):
	op1 = do_op1(x[i], y[i], z[i])
	op2 = do_op2(op1, y[i])
	op3 = do_op3(op2)
	final_result.append(op3)


final_sum = delayed(sum)(final_result)
final_sum.compute()
final_sum.visualize()
```
