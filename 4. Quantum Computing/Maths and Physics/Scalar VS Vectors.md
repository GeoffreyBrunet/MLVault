**MOC**:: [[4. Quantum Computing MOC]]
**Tags**:: #quantum #maths 

# Differences
- Scalars => magnitude
	- Distance is scalar quantity notated $s$.
	- Speed is a scalar.
	- Mass is a scalar.
	- Temperature is a scalar.
- Vectors => magnitude + direction
	- Displacement is a vector notated $\overrightarrow{x}$.
	- Velocity is a vector notated $\overrightarrow{v}$ who is derivative of displacement divided by derivative of time: $\overrightarrow{v} = \frac{\partial \overrightarrow{x}}{\partial t}$.
	- Acceleration is a vector notated $\overrightarrow{a}$ and $\overrightarrow{a} = \frac{\partial \overrightarrow{v}}{\partial t}$.
	- Forces (from second law of newton) are vectors notated $\overrightarrow{f}$ and $\overrightarrow{f}=m\cdot\overrightarrow{a}$.

In physics, a physical quantity can be defined by a scalar or a vector. The product between a scalar and a vector is always a vector.

# Vectors

## Example in 2D world
On 2D plane where:
- $x$ = equal to $2$.
- $y$ = equal to 3
- $\overrightarrow{r}$ = arrow from rooted to coordonates.
$$
\overrightarrow{r} = 2\hat{x}+3\hat{y} =
\begin{pmatrix}
2 \\ 3
\end{pmatrix}
$$ 

# Matrices
## Links
- For matrices, see: [[Matrices]]
- For martrix multiplication, see: [[Matrix multiplication]]
- For transposing matrix, see: [[Transpose vector or matrix]]
## Dagger
Dagger is defined as the complex conjugate transposition of a matrix.
$$
A^{\dagger} = (\overline{A})^{t}
$$
**Example 1** :
Let have matrix:
$$
\psi = 
\begin{pmatrix}
\frac{i}{\sqrt{2}} \\
0 \\
0 \\
\frac{i}{\sqrt{2}}
\end{pmatrix}
$$
Now compute **phi** matrix dagger:
$$
\psi^{\dagger} = \psi = 
\begin{pmatrix}
\frac{i}{\sqrt{2}} &
0 &
0 &
\frac{i}{\sqrt{2}}
\end{pmatrix}
$$
**Example 2** :
Let have matrix:
$$
A = 
\begin{pmatrix}
i & 0 \\
-3i & 4
\end{pmatrix}
$$
Now compute **phi** matrix dagger:
$$
A^{\dagger} = \begin{pmatrix}
-i & +3i \\
0 & 4
\end{pmatrix}
$$
