**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definitions
**Polynomial** is a function that as an unknown, a coefficient and some power.
**Notations** of derivatives:
- $\frac{d}{dx}$
- $f'$ for a function $f$

Derivatives point int the direction of increases and decreases in a mathematical function.

In DL, the goal (e.g., classification) is represented as an error function. Thus, the best solution is the point with the smallest error. The derivative tells us which way to "move" in that error landscape in order to find the optimal solution.

# Formula
Formula for derivative a polynomial is:
$$
\frac{d}{dx}\textcolor{orange}{a}\textcolor{blue}{x}^\textcolor{green}{n} = \textcolor{green}{n}\textcolor{orange}{a}\textcolor{blue}{x}^{\textcolor{green}{n}-1}
$$


# Maths examples
## Example 1, derivative of $x^2$
$$
\frac{d}{dx}x^2 = 2x^1
$$
## Example 2, derivative of $x^3$
$$
\frac{d}{dx}x^3 = 3x^2
$$
## Example 3, derivative of $3x^3$
$$
\frac{d}{dx}3x^3 = 9x^2
$$

# Python example
```python
import numpy as np
# sympy is simbolic math in python
import sympy as sym
import sympy.plotting.plot as symplot

x = sym.symbols('x')
fx = 2*x**2
df = sym.diff(fx, x)

symplot(fx, (x, -4, 4), title='The function')
symplot(df, (x, -4, 4), title='Its derivative')
```
