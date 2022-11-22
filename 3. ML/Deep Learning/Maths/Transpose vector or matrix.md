**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definition
Let $A$ be a matrix of $n$ rows and $p$ columns, whose coefficients are $a_{i,j}$. The transpose of $A$ denoted $^tA$ is the matrix of $n$ rows and $p$ columns, whose coefficient of the $i$th row and $j$th column is $a_{i,j}$. In other words, we swap the role of rows and columns.

# Examples
## Vector example
$$
\begin{pmatrix}
1 \\
0 \\
2 \\
5 \\
-2
\end{pmatrix}^T
=
\begin{pmatrix}
1 \ 0 \ 2 \ 5 \ -2
\end{pmatrix}
$$
## Matrix example
$$
\begin{pmatrix}
1 & 5 \\
0 & 6 \\
2 & 8 \\
5 & 3 \\
-2 & 0
\end{pmatrix}^T
=
\begin{pmatrix}
1 & 0 & 2 & 5 & -2 \\
5 & 8 & 6 & 3 & 0
\end{pmatrix}
$$

# Code examples
## Numpy example
```python
import numpy as np

# Create vector
nv = np.array([1, 0, 2, 5, -2])

# Transpose it
nv.T
```
## Pytorch example
```python
import torch

tv = torch.tensor([ [1, 2, 3, 4] ])
tv.T
```
