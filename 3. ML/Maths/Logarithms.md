**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## Usefulness
The logarithm or the log function or the log transform is really important in machine learning and in optimization. ML (and thus DL) often involve minimizing small quantities like probabilities (computers suffer from precision errors when working with very small numbers). So the idea is that just stretch out those numbers and that just makes the optimization code work better.

## Definition & notes
- Logarithm is the inverse of the natural exponential (aka [Euler number](https://en.wikipedia.org/wiki/E_(mathematical_constant))).
- $log(exp(x))$ where x is a number, return a line with same numbers as coordinates (ex: -1 and -1, 0 and 0, 10 and 10).
- $log$ function is monotonic, it means that whenever X goes up, the log also goes up and when X goes down, the log goes down.
- $log$ stretches small values of X, and better distinguishes small and closely spaced numbers.
- That fits in nicelly with using sigmoid functions and [[Softmax]] functions.
### Logs with different bases
- `ln` is notation for log base (Natural Log).
- Others are written $log2$ or $log10$ by example.
- All $log$ have the same properties.
- They differ in slope.
- Natural Log (ln) is often used because of its relation to $e$.

## Numpy example
```python
import numpy as np

# np.linspace create 1D array from .0001 to 1 with 200 elements.
x = np.linspace(.0001, 1, 200)
logx = np.log(x)
```
