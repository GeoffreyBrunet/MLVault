**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## Examples
$\textcolor{blue}{min}$ is the smallest value.
$$
\textcolor{blue}{min}\{1, -1, 3, 0, 4, 3\} = \textcolor{blue}{-1}
$$
$\textcolor{orange}{max}$ is the largest value.
$$
\textcolor{orange}{max}\{1, -1, 3, 0, 4, 3\} = \textcolor{orange}{4}
$$
$\textcolor{blue}{argmin}$ is the location of this smallest value.
$$
\textcolor{blue}{argmin}\{1, -1, 3, 0, 4, 3\} = \textcolor{blue}{2}
$$
$\textcolor{orange}{argmax}$ is the location of this largest value.
$$
\textcolor{orange}{argmax}\{1, -1, 3, 0, 4, 3\} = \textcolor{orange}{5}
$$

## Formulas
### Argmax formula
$$
z = \underset{\textcolor{blue}{x}}{\operatorname{argmax}} f(\textcolor{blue}{x})
$$
$\textcolor{blue}{x}$ under argmax means we are maximizing over $x$, we are finding the positions in $x$ at which this function is maximum.

## Code examples
### Numpy example
#### on vector
```python
import numpy as np

v = np.array([1, 40, 2, -3])

minval = np.min(v)
maxval = np.max(v)

minidx = np.argmin(v)
maxidx = np.argmax(v)
```
#### ON matrix
```python
import numpy as np

M = np.array([[0, 1, 10], [20, 8, 5]])

minvals1 = np.min(M) # min on all matrix
minvals2 = np.min(M, axis=0) # min on each column
minvals3 = np.min(M, axis=1) # min on each row
maxvals1 = np.max(M) # max on all matrix
maxvals1 = np.max(M, axis=0) # max on each column
maxvals1 = np.max(M, axis=1) # max on each row

minidx1 = np.argmin(M)
minidx2 = np.argmin(M, axis=0)
minidx3 = np.argmin(M, axis=1)
maxidx1 = np.argmax(M)
maxidx2 = np.argmax(M, axis=0)
maxidx3 = np.argmax(M, axis=1)
```
### Pytorch example
#### on vector
```python
import torch

v = torch.tensor([1, 40, 2, -3])

minval = torch.min(v)
maxval = torch.max(v)
```
#### on matrix
```python
import torch

M = torch.tensor([[0, 1, 10], [20, 8, 5]])

# min and max in pytorch return a specific type: torch.return_types.min or .max
minvals1 = torch.min(M) # min on all matrix
minvals2 = torch.min(M, axis=0) # min on each column
minvals3 = torch.min(M, axis=1) # min on each row
maxvals1 = torch.max(M) # max on all matrix
maxvals1 = torch.max(M, axis=0) # max on each column
maxvals1 = torch.max(M, axis=1) # max on each row

# Returns a namedtuple `(values, indices)` where `values` is the minimum value of each row of the `input` tensor in the given dimension `dim`. And `indices` is the index location of each minimum value found (argmin).
minvals1.values
minvals1.indices
```
More doc at: [torch.min documenation](https://pytorch.org/docs/stable/generated/torch.min.html).
