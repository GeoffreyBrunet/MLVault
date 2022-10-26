**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## About
- Derivatives of "interacting" functions (multiplications and embeddings) is unintuitive.
- In practice, librairies like PyTorch, Tensorflow, etc., have routines that estimate complicated derivatives very efficiently and accurately.

## Product rule of derivatives of multiple functions
### Formula
For multiplications:
$$
(f \times G)' = f'\times g + f \times g'
$$

### Code example
```python
import numpy as np
import sympy as sym

# create symbolic variables in sympy
x = sym.symbols('x')

# create two functions
fx = 2*x**2
gx = 4*x**3 - 3*x**4

# compute their individual derivatives
df = sym.diff(fx)
dg = sym.diff(gx)

# apply the product rule "manually"
manual = df*gx + fx*dg
thewrongway = df*dg

# via sympy
viasympy = sym.diff( fx*gx )
```

## Chain rule of derivatives of embedded functions
### Formula
$$
\frac{df}{dx}f(g(x)) = f'(g(x))\times g'(x)
$$

### Example
$$
\frac{df}{dx}(x^2 + 4x^3)^5  = 5(x^2 + 4x^3)4 \times (2x + 12x^2)
$$

### Code example
```python
import numpy as np
import sympy as sym

# create symbolic variables in sympy
x = sym.symbols('x')

# create two functions
fx = 2*x**2
gx = 4*x**3 - 3*x**4

# # create two functions with chain rule
gx = x**2 + 4*x**3
fx = ( gx )**5

# apply the product rule via sympy
sym.diff(fx)
```
