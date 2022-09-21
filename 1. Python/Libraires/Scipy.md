**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library
## Definition
**SciPy** is not just a library, but a whole **ecosystem** of libraries that work together to help you accomplish complicated scientific tasks quickly and reliably.
## Code notes
Scipy can compute linear algebrea algorithms on [[Numpy]] `ndarray`. Here get determinant of matrix (ndarray).
```python
import numpy as np
import scipy.linalg as lg

my_sqr_matrix = np.array([[1, 2, 3], [4, 15, 6], [17, 8, 9]])
lg.det(my_sqr_matrix)
# Return -450.0
```
A lot of other scientific computing algorithms can be found on [Scipy's API documentation](https://docs.scipy.org/doc/scipy/reference/index.html).
