**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## Types of multiplication
### Product of a matrix by a real number
Let $A$ be a matrix and $k$ a real number. The product $kA$ is the matrix obtained by multiplying each coefficient of $A$ by $k$.
### Produit de deux matrices
Let $A=(a_{ij})$ be a $n$cdot p$ matrix and $B=(b_{ij})$ a $p\cdot q$ matrix. The product of $A$ and $B$ is the $C=(c_{ij})$ matrix with $n$ rows and $q$ columns whose coefficient in the $i$th row and $j$th column is obtained by multiplying the $i$th row of $A$ by the $j$th column of $B$.
> The number of columns of the first matrix must be equal to the number of rows of the second matrix for the calculation to be possible. For example, the product of a matrix $2\cdot \textcolor{red}{3}$ by a matrix $\textcolor{red}{3}\cdot 4$ is possible and gives a matrix $2\cdot4$.

$$
C = \begin{pmatrix} \textcolor{red}{2} & \textcolor{red}{4}\\ 1 & 0 \end{pmatrix} \cdot \begin{pmatrix} \textcolor{red}{-1} & 0 & 2 \\ \textcolor{red}{-2}& 1 & 0 \end{pmatrix} = \begin{pmatrix} \textcolor{red}{-10} & \cdots & \cdots \\ \cdots & \cdots & \cdots \end{pmatrix}
$$
Let $A, B, C$ be three square matrices of the same dimension.
-   $A×(B+C)=A×B+A×C$ (Left distributivity)
-   $(A+B)×C=A×C+B×C$ (Right distributivity)
-   $A×(B×C)=(A×B)×C$ (associativité de la multiplication)
-   $A×B≠B×A$ : la multiplication n'est **pas** commutative.

## Numpy example
```python
import numpy as np

# Create matrices
a = np.random.randn(3, 4)
b = np.random.randn(4, 5)

# Dot product, "@" is Python's Matrix Multiplication Operator
np.round(a@b, 2)
```
