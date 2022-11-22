**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definition
A **matrix** of dimension (or *order* or *size*) $n$cdot p$ is an array of real numbers (called coefficients or terms) with $n$ rows and $p$ columns.

In short, $A=(a_{ij})$ is the matrix whose coefficient in the $i$th row and $j$th column is $a_{ij}$.

- A **square** matrix is a matrix whose number of rows is equal to the number of columns.
- A **row** matrix is a matrix whose number of rows is equal to 1.
- A **column** matrix is a matrix whose number of columns is equal to 1.
- For a square matrix, we call **main diagonal**, the diagonal that connects the upper left corner to the lower right corner.
- The **null** matrix of dimension $n \cdot p$ is the matrix of dimension $n \cdot p$ for which all coefficients are null.
- A **diagonal** matrix is a square matrix whose coefficients outside the main diagonal are zero.
- The **unitary** matrix of dimension $n$ is the square matrix of dimension $n$ which contains 1's on the main diagonal and 0's elsewhere.

# Operations on matrices
## Sum of matrices
Let $A$ and $B$ be two matrices of the same dimension. The sum $A + B$ of the matrices $A$ and $B$ is obtained by adding the coefficients of $A$ to the coefficients of $B$ located **at the same position**.


## Product of a matrix by a real number
Let $A$ be a matrix and $k$ a real number. The product $kA$ is the matrix obtained by multiplying each of the coefficients of $A$ by $k$.


## Product of a row matrix by a column matrix
Let $$A = 
\begin{pmatrix}
a_{1} & a_{1} & \cdots & a_{n} \\
\end{pmatrix}$$ a row matrix $1cdot n$ and
$$B = \begin{pmatrix}
b_1 \\
b_2 \\
\cdots \\
b_n
\end{pmatrix}
$$ a column matrix $n \cdot 1$. The product of $A$ and $B$ is a real number:

$$
A \cdot B = \begin{pmatrix}
a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
\end{pmatrix} \cdot \begin{pmatrix}
b_1 \\
b_2 \\
\cdots \\
b_n
\end{pmatrix} = a_1 \cdot b_1 + a_2 \cdot b_2 + \cdots + a_n \cdot b_n
$$
> The two matrices must have the same number $n$ of coefficients. The row matrix must be first.


## Power of a matrix
Let $A$ be a square matrix and $n$ a natural number. Let $A^n$ be the matrix:
$A^n = A×A×cdots×A$ ($n$ factors).
> By convention, we will consider that $A^0$ is the unit matrix of the same size as $A$.


## Transpose matrix
Let $A$ be a matrix of $n$ rows and $p$ columns, whose coefficients are $a_{i,j}$. The transpose of $A$ denoted $^tA$ is the matrix of $n$ rows and $p$ columns, whose coefficient of the $i$th row and $j$th column is $a_{i,j}$. In other words, we swap the role of rows and columns.


## Invertible matrix
A square matrix $A$ of dimension $n$ is **invertible** if and only if there exists a matrix $B$ such that $A×B=B×A=I_n$ where $I_n$ is the unit matrix of dimension $n$. The formula to calculate it is:
$$
A^{-1} = \frac{1}{det(A)} . ^Tcom(A)
$$

## Identity matrix
The **identity matrix** of dimension $ncdot n$, denoted $I_n$ is a square matrix of $n$ rows and $n$ columns. All the elements of its diagonal are equal to $1$ and all the other elements are equal to $0$. The formula for computing an identity matrix is: $I = M^{-1}\cdot M$.
