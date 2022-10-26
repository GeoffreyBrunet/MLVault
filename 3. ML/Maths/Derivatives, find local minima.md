**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #maths 

## About
The main purpose of computing derivatives in the gradient descent algorithm is to identify **local minima**.

Compute maxima and minima:
- Get function.
- Compute derivative of this function.
- Set derivative to zero for compute $x$.
- Compute $x$.

Variations for $f(x)'$ :
- If the derivative is strictly positive on an interval, the function is strictly increasing on this interval: $f'> O: f\nearrow$: 
- If the derivative is strictly negative on an interval, the function is strictly decreasing on this interval $f'< O: f\searrow$
 
Minima and maxima have $df=0$.
Minima have $df<0$ to the left, and $df>0$  to the right.
Maxima have $df>0$ to the left, and $df<0$  to the right.

## Math example
1. Get function
$$
f(x) = -x^4+3x^2
$$
2. Compute derivative of this function
$$
\frac{df}{dx} = -4x^3+6x
$$
3. Set derivative to zero for compute $x$
$$
-4x^3+6x=0
$$
4. Compute $x$
$$
x=0,\pm \sqrt{3/2}
$$
## Vanishing gradient
The function is that a flat area, the function is continuing are constant here. It's a problem for deep learning called vanishing gradient.

It describes the situation where a deep multilayer feed-forward network or a recurrent neural network is unable to propagate useful gradient information from the output end of the model back to the layers near the input end of the model.
