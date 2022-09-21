**MOC**:: [[1. Python MOC]]
**Tags**:: #python #language
## Definition
- Basically C code with Python.
- It allows to use C data types, functions, modules, and so on within the Python code.
- Basically translate our code to an optimized version of C code, which can be combined with Python code.
- It's a superset of Python (barring a few exceptional cases).
## Workflow
- Translate code written in Python.
- Compile the code.
- Bundle it to Python Extensions
- Use the bundled Python extension in your existing Python code.
## Code notes
### Installation
```shell
pip install Cython
```
### Hello World in Cython
Cython code use **.pyx** extension. Create `hello.pyx` file with this body:
```cython
print("Hello, World!")
```
And call it in new `setup.py` Python's script:
```python
from setuptools import setup
from Cython.build import cythonize

setup(ext_modules=cythonize("hello.pyx"))
```
and compile with this command:
```shell
python setup.py build_ext --inplace
```
and now in **Python interpreter**, can use `hello` package:
```python
import hello
# Print Cython string as output
```
### Use Cython in Jupyter notebook
To use Cython in the Jupyter Notebook, we first need to import the Cython Jupyter extension:
```ipynb
%load_ext cython
```
and in a Cython cell, add cython's prefix:
```ipynb
%%cython
```
### Define function
**Python functions** are defined using the `def` statement, as in Python. They take Python objects as parameters and return Python objects.
**C functions** are defined using the new `cdef` statement. They take either Python objects or C values as parameters, and can return either Python objects or C values.
**Hybrid functions** are defined using `cpdef` statement. `cpdef` functions combine both `def` and `cdef` by creating two functions; a `cdef` for C types and a `def` for Python types.
> Within a Cython module, Python functions and C functions can call each other freely, but only Python functions can be called from outside the module by interpreted Python code. So, any functions that you want to "export" from your Cython module must be declared as Python functions using def.

Python function with C types
```cython
%%cython
def factorial_cyData(n):
	cdef int fact = 1
	cdef int x
	for x in range(2, n+1):
	fact = fact * x
	return fact
```
or Cython pure function:
```cython
%%cython
cdef factorial_cyData(n):
	cdef int fact = 1
	cdef int x
	for x in range(2, n+1):
	fact = fact * x
	return fact
```
### Cython data types
- Integer types:
	- Long
	- Int
	- Unsigned short
	- Unsigned long, and so on
- Floating types:
	- Float
	- Double
- String types
- Complex types
- Untyped objects
**Typed variable** can be declared in Cython code using cdef keyword, and type, few examples here:
```cython
# Int type variables
cdef int x = 0
cdef long y = 1
cdef unsigned long z = 100

# Float type variables
cdef double x_db = 1.11
cdef float y_f = 2.04

# String variables
cdef str my_str = "hello"

# Complex type variables
cdef double complex my_complex = 100 + 50j

# Untyped variables (dynamically changed at runtime)
my_var = 1
my_var = 'abc'
my_var = [1, 2, 3]
```
