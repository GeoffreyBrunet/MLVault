**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library

# Definition
[Numba](https://numba.pydata.org) is a Just In Time (JIT) compiler for accelerating Python code. It translate Python code to optimized version of machine code at runtime using [LLVM](https://llvm.org) compiler. Unlike Cython, it does not require any additional language extensions. It's focused more on numerical code like computations involving int, float, double and so on. It can be use on GPU for more optimizations.

# Using
Use `@jit` [[Decorator]] to speedup existing Python code using Numba's JIT compiler. `@jit(parallel=True)` can enable threading on actually Python code. Support for Nvidia's GPUs for enhanced performance works, but is experimental on AMD's GPUs. Depending on CPU, loops are translated into vector instructions.

# Unsupported code
- Explicit `**kwargs`
- Key argument in sorted function
- Coroutines using genetators
- Nested lists was not supported till version 0.39.0
Check supported features on [this documentation](https://numba.pydata.org/numba-doc/dev/reference/numpysupported.html).

# Modes
## nopython mode:
- Code compiled in this mode does not access Python.
- If for some reason, code cannot be compiled in this mode, compilation switches to **Object mode**.
- Highest performances in this mode.
- Can be use with `@jit(nopython=True)` or `@njit` annotation.
## Object mode:
- Default compilation mode, which use Python C API only without any optimizations.

# Numpy universal functions
A universal function in Numpy operates on Numpy arrays elements wise. They support broadcasting and other standard features of Numpy arrays. Universal functions in Numba can be created using `@vectorize` decorator.

# Threading
In Numba, there is two ways to use threading:
- using as parameter: `@jit(parallel=True)` or `@njit(parallel=True)`
- using as parameter: `@vectorize(parallel=True)`
Three types of threading layers avaible:
- workqueue
- tbb (Intel threading building blocks)
- omp (openMP)
More on [this documentation](https://numba.pydata.org/numba-doc/latest/user/threading-layer.html).

# Code examples
Numba functions can have typed I/O defined in code. In this example, function return one `float64` array and take two `float64` array as input.
```python
from numba import float64, jit

numba_fast = jit(float64[:](float64[:], float64[:]), nopython=True)(some_function)
```
