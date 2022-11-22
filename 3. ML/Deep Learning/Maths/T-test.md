**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# General idea
A t-test is a **statistical test** that is used to compare the [[Mean]]s of two groups. It is often used in **hypothesis testing** to determine whether a process or treatment actually has an effect on the population of interest, or whether two groups are different from one another.

# Basic formula
$$
t_k=\frac{\bar{x}-\bar{y}}{s/\sqrt{n}}
$$

- $t_k$ is the single result value.
- $\bar{x}$ and $\bar{y}$ are means of two sets.
- $s/\sqrt{n}$ is the [[Standard deviation]].
- $n$ correspond the number of time that we repeat the model, root-square is here for normalize it.
Simply resumed, formula is:
$$
t_k = \frac{\text{a}}{\text{Standard deviation}}
$$

# Python examples
## Example with numpy and scipy
```python
import numpy as np
import scipy.stats as stats

# parameters
n1 = 30 # samples in dataset 1
n2 = 40 # ...and 2
mu1 = 1 # population mean in dataset 1
mu2 = 2 # population mean in dataset 2

# generate the data
data1 = mu1 + np.random.randn(n1)
data2 = mu2 + np.random.randn(n2)

# _ind = independent samples
t,p = stats.ttest_ind(data1,data2)
print(t)
print(p)
```
