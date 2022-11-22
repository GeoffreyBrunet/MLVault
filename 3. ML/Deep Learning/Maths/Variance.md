**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definition and formula
The variance is a measure of the dispersion of all values in a data set. It is the most commonly used measure of dispersion.
The mathematical formula for the variance is therefore the following:
$$
V(x) = (\sum_{i=1}^{p} n_i x_i^2-x^{-2}) \times \frac{1}{n}
$$
or:
$$
\sigma^{2} = \frac{1}{n-1}\sum^{n}_{i=1}(x_{i}-\bar{x})^{2}
$$
For second formula, value and mean are squared because we want the variance to indicate the dispersion around the mean. It's also usefull for taking derivatives, calculus and nice geometric properties.

Variance is suitable for
- any distribution.
Suitable data types:
- numerical
- ordinal (but require [[Mean]]).

# Example
Let's calculate the variance of the following set: $2, 7, 3, 12, 9$.
- The first step is to calculate the mean. The sum is 33 and there are 5 numbers. The mean is $33 ÷ 5 =6.6$. Next, we need to calculate the squared deviation between each value and the mean. For example for the first value: $(2-6,6)^2 = 21,16$
- The squared deviations of each value are then added together: $21,16 + 0,16 + 12,96 + 29,16 + 5,76 = 69,20$
- This sum is then divided by the number of values, which is: $69,20 ÷ 5 = 13,84$
The variance is therefore $13.84$.

# Mean Absolute difference
$$
\sigma^{2} = \frac{1}{n-1}\sum^{n}_{i=1}\lvert x_{i}-\bar{x}\rvert
$$
This is the same formula as Variance but we don't take squares, we take absolute values.
**Squaring**: emphasizes large values; it's better for optimization (continous and differentiable); is closer to Euclidian distance; is the second "moment" of the distribution; better link to least-squares regression.
**MAD**: also good, robust to outliers, less commonly used.

# Code examples
## Numpy example
```python
import numpy as np

x = [1, 2, 4, 6, 5, 4, 0]
n = len(x)

# ddof is here for remove bias
variance = np.var(x, ddof=1)
# or vanilla:
vanilla_variance = (1/(n-1)) * np.sum((x - np.mean(x))**2)
```

