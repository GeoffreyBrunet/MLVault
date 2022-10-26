**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## Definition
A single number that reflects the commonolalities between two objects (vectors, matrices, tensors, signals, images).

## Applications
- **Statistics**: correlation, least-squares, entropy, PCA
- **Signal processing**: fourier transform, filtering
- **Science**: geometry, physics, mechanics
- **Linear algebra**: projection, transformations, multiplication
- **Deep learning**: convolution, matrix multiplication, Gram matrix (used in style transfer)

## Various notations
$$
\alpha = a \cdot b = \langle a,b \rangle = a^Tb = \sum_{i=1}^{n} a_i b_i
$$
Here $a$ and $b$ are both two vectors with same dimension. $a^Tb$ is the most common notation.

## Examples
### Dot product of vector
$$
a = \begin{pmatrix}
1 \\
0 \\
2 \\
5 \\
-2
\end{pmatrix}
b = \begin{pmatrix}
2 \\
8 \\
-6 \\
1 \\
0
\end{pmatrix}
$$
$$
\begin{split}
a^Tb = 1\cdot2 + 0\cdot8 + 2\cdot(-6) + 5\cdot1 + (-2)\cdot0 \\
a^Tb = 2 - 12 + 5 \\
a^Tb = -5
\end{split}
$$
### Dot product of 2D matrix (3x3)
$$
a = \begin{pmatrix}
0 & 3 & 2 \\
-3 & -3 & 1 \\
1 & 0 & 1
\end{pmatrix}
b = \begin{pmatrix}
1 & 0 & 6 \\
2 & -1 & 0 \\
5 & 1 & 4
\end{pmatrix}
$$
$$
\begin{split}
a^Tb = 0\cdot1 + 3\cdot0 + 2\cdot6 \\
+ -3\cdot2 + -3\cdot-2 + 1\cdot0 \\
+ 1\cdot5 + 0\cdot1 + 2\cdot4 \\
a^Tb = 0 + 0 + 12 + -6 + 3 + 0 + 5 + 0 + 8 \\
a^Tb = 22
\end{split}
$$

## Code examples
### Numpy example
```python
import numpy as np

# Create vector
a = np.array([1, 0, 2, 5, -2])
b = np.array([2, 8, -6, 1, 0])

# Dot product
np.dot(a, b)
```
### Pytorch example
```python
import torch

tv1 = torch.tensor([1, 2, 3, 4])
tv2 = torch.tensor([0, 1, 0, -1])
torch.dot(tv1, tv2)
```
