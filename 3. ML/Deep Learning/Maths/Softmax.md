**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Formula
$$
\sigma_i = \frac{e^{z_i}}{\sum e^z}
$$
Where:
- $e$ is [Euler number](https://en.wikipedia.org/wiki/E_(mathematical_constant))
- $z$ is a collection of numbers (a vector)
## Numerical example
$$
\begin{split}
z = \{1, 2, 3\} \\
e^z = \{2.72, 7.39, 20.01\} \\
\sum e^z = 30.19 \\
\sigma = \{.09, .24, .67\}
\end{split}
$$
- Sum of numbers in set after being passed through softmax function is always going equel to one.
- All values are include between 0 to 1.

# Code examples
## Numpy example
```python
import numpy as np

z = [1, 2, 3]

num = np.exp(z)
den = np.sum(np.exp(z))
sigma = num / den
```
## Pytorch Example
```python
import torch
import torch.nn as nn

z = [1, 2, 3]
softfun = nn.Softmax(dim=0)
sigmaT = softfun(torch.Tensor(z))
```