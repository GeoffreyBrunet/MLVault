**MOC**:: [[4. Quantum Computing MOC]]
**Tags**:: #quantum #maths 

# Formula
Let have 2 matrices,
- $A$ who have $m\times n$ dimensions
- $B$ who have $p\times q$ dimensions.
$$
A \otimes B = C
$$
So:
$$
(m\times n) \otimes(p\times q) = (m\cdot p \times n \cdot q)
$$

# Examples
## Example 1:
Let have 2 matrices $A$ and $b$:
$A = \begin{pmatrix}1 & 2 \\3 & 4\end{pmatrix}$ and $B = \begin{pmatrix}1 & 1 \\1 & 2\end{pmatrix}$:
So tensor product is:
$$
A \otimes B = 
\begin{pmatrix}
1 \begin{vmatrix}
1 & 1 \\
1 & 2
\end{vmatrix} &
2 \begin{vmatrix}
1 & 1 \\
1 & 2
\end{vmatrix} \\
3 \begin{vmatrix}
1 & 1 \\
1 & 2
\end{vmatrix} &
4 \begin{vmatrix}
1 & 1 \\
1 & 2
\end{vmatrix}
\end{pmatrix}
$$
$$
A \otimes B = 
\begin{pmatrix}
\begin{matrix}
1 & 1 \\
1 & 1
\end{matrix} &
\begin{matrix}
2 & 2 \\
2 & 4
\end{matrix} \\
\begin{matrix}
3 & 3 \\
3 & 6
\end{matrix} &
\begin{matrix}
4 & 4 \\
4 & 8
\end{matrix}
\end{pmatrix}
$$
Tensor product of 2 matrix with $2 \times 2$ dimensions create a new matrix with $4 \times 4$ dimensions.

## Example 2:
Let have 2 matrices $A$ and $b$:
$\psi_1 = \begin{pmatrix}0 \\1\end{pmatrix}$ and $\psi_2 = \begin{pmatrix}1 \\0\end{pmatrix}$:
So tensor product is:
$$
\psi_1 \otimes \psi_2 = 
\begin{pmatrix}
0 \begin{vmatrix}
1 \\ 0
\end{vmatrix} \\
1 \begin{vmatrix}
1 \\ 0
\end{vmatrix}
\end{pmatrix} =
\begin{pmatrix}
0 \\ 0 \\ 1 \\ 0
\end{pmatrix}
$$
Tensor product of 2 matrix with $2 \times 1$ dimensions create a new matrix with $4 \times 1$ dimensions.
