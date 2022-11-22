**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #activationfunction 

# Definition & notes
 Sigmoid function exists between **(0 to 1).** Therefore, it is especially used for models where we have to **predict the probability** as an output.Since probability of anything exists only between the range of **0 and 1,** sigmoid is the right choice.

The function is **differentiable**.That means, we can find the slope of the sigmoid curve at any two points.

The function is **monotonic** but function’s derivative is not.

The Sigmoid Function curve looks like a S-shape.

# Formula
$$
\sigma(x) = \frac{1}{1+e^{z}}
$$

# Python example
```python
import sympy as sym

sigmoid = 1 / (1+sym.exp(-x))
p = symplot(sigmoid,(x,-4,4),label='Sigmoid',show=False,line_color='red')
p = symplot(sym.diff(sigmoid),(x,-4,4),label='df(Sigmoid)',show=False,line_color='red')
```
