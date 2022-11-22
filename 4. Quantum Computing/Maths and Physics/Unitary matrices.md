**MOC**:: [[4. Quantum Computing MOC]]
**Tags**:: #quantum #maths 

> Definition of unitary matrix in: [[Matrices]].
> **Unitary matrices** are important because in quantum computing, **quantum gates** are represented by them.

# Formula
$$
U^{\dagger}U = U \cdot U^{\dagger} = I
$$
$I$ is the identity matrix and $U$ is a square matrix.

# Trace
Trace of square matrix is notated $\Tr(A)$ and is defined as the sum of the diagonal elements.
## Examples:
### Example 1:
$$
x = \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$
So trace is:
$$
\Tr(x) = 0+0
$$
### Example 2:
$$
A = \frac{1}{\sqrt{2}}\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
$$
So trace is:
$$
\Tr(A) = \frac{1}{\sqrt{2}} - \frac{1}{\sqrt{2}} = 0
$$
### Example 3:
$$
I = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$
So trace is:
$$
\Tr(I) = 1+1 = 2
$$
### Example 4:
$$
A = \begin{vmatrix}
1 & 0 & 3 \\
11 & 5 & 2 \\
6 & 12 & 5
\end{vmatrix}
$$
So trace is:
$$
\Tr(A) = 1+5+5 = 11
$$
