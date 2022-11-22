**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definition and formula
The mean is the most commonly used mesure of central tendency, and the idea of central tendency is one number, one value that tells us something about the concentration of the data in a distribution.
The "mean" value is equal to the **quotient of the sum of all the values** in the series **divided by the total number of people**. It is always noted: $\bar{x}$.

**Formula** is:
$$
\bar{x} = n^{-1}\sum^{n}_{i=1}x_{i}
$$
**Notations** are: $\bar{x} = \mu = \mu_{x}$.

Mean is suitable for:
- roughly normally distributed data.
Suitable data types:
- interval
- ratio

# Code examples
## Numpy example
```python
import numpy as np

x = [1, 2, 4, 6, 5, 4, 0]
n = len(x)

mean = np.mean(x)
# or vanilla:
vanilla_mean = np.sum(x) / n
```
