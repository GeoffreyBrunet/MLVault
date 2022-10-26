**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## Utility
On computer, exactly reproduce the same set of random numbers, and it's done with a procedure called **seeding** or **random number generation seeding**. It's usefull when initialize models, we can keep the same initial random state (random weights at start).

## Python examples
### Numpy example
```python
import numpy as np

np.random.seed(0)
np.random.rand(5)
```
### PyTorch Example
```python
import torch

torch.manual_seed(0)
torch.randn(5)
```
Documentation here: [PyTorch reproducible randomness](https://pytorch.org/docs/stable/notes/randomness.html).