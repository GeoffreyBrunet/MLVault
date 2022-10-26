**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #activationfunction 

## Definition & notes
The ReLU is half rectified (from bottom). f(z) is zero when z is less than zero and f(z) is equal to z when z is above or equal to zero.

**Range**:  0 to infinity.

The function and its derivative **both are** **monotonic**.

## Python example
```python
import sympy as sym

relu = sym.Max(0, x)
p = symplot(relu,(x,-4,4),label='ReLU',show=False,line_color='blue')
p = symplot(sym.diff(relu),(x,-4,4),label='df(ReLU)',show=False,line_color='blue')
```
