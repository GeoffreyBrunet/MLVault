**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Formula

$$
H(\textcolor{brown}{p}) = -\sum \textcolor{brown}{p}\log(\textcolor{brown}{p})
$$
**[[Entropy]]** describes one probability distribution.
$$
H(\textcolor{brown}{p}, \textcolor{orange}{q}) = -\sum \textcolor{brown}{p}\log(\textcolor{orange}{q})
$$
**Cross-entropy** describes the relationship between two probabilities distributions.

# Code examples
## Numpy example
```python
p = [1, 0] # sum = 1
q = [0.25, 0.75] # sum = 1

H = 0
for i in range(len(p)):
	H -= p[i]*np.log(q[i])
```
## Pytorch example
```python
import torch
import torch.nn.functional as F

p_tensor = torch.Tensor(p)
q_tensor = torch.Tensor(q)

F.binary_cross_entropy(p_tensor, q_tensor)
```