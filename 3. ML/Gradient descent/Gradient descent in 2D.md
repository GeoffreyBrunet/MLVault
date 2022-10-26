**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #gradientdescent 

## About
### Partial derivatives
Partial derivatives are the derivatives of the function, ignoring one dimension and only focusing on the other dimension. So the partial derivative with respect to X means that we ignore Y and we just see how is the function changing other X and similar thought Y. In two dimensions, we have 2 partial derivatives.

### Gradient
The gradient of the functionat any given point is just a collection of all the partial dérivatives with respect to all the dimensions of that function.

## Notations
### Derivative
$$
\frac{\textcolor{blue}{d}f}{\textcolor{blue}{d}x} = f\textcolor{blue}{'}(x) = \textcolor{blue}{d}f
$$

### Partial derivative
$$
\frac{\textcolor{blue}{\partial} f}{\textcolor{blue}{\partial} x} = f_{\textcolor{blue}{x}}(x) = \textcolor{blue}{\partial_x}f
$$

### Gradient
$$
\textcolor{blue}{\nabla} = (\textcolor{blue}{\partial_x}f, \textcolor{blue}{\partial_y}f, \cdots, \textcolor{blue}{\partial_z}f)
$$

## Example
**Example for this function**
$$
f(x, y)=3(1-x)^2e^{-x^2-(y+1)^2}-10(\frac{x}{5}-x^3-y^5)e^{-x^2-y-2}-\frac{1}{3}e^{(x+1)^2-y^2}
$$
**Python code**
There are 3 main steps:
- Compute the partial derivative of the function
- Repeat gradient descent loop
- Note that the local minima is (x, y).
```python
import numpy as np
import matplotlib.pyplot as plt
import sympy as sym # sympy to compute the partial derivatives

# the "peaks" function
def peaks(x,y):
	# expand to a 2D mesh
	# the numpy.meshgrid function is used to create a rectangular grid
	x,y = np.meshgrid(x,y)
	z = 3*(1-x)**2 * np.exp(-(x**2) - (y+1)**2) \
		- 10*(x/5 - x**3 - y**5) * np.exp(-x**2-y**2) \
		- 1/3*np.exp(-(x+1)**2 - y**2)
	return z

# create the landscape
x = np.linspace(-3,3,201)
y = np.linspace(-3,3,201)
Z = peaks(x,y)
# let's have a look!
plt.imshow(Z,extent=[x[0],x[-1],y[0],y[-1]],vmin=-5,vmax=5,origin='lower')
plt.show()

# create derivative functions using sympy
sx,sy = sym.symbols('sx,sy')

# rewrite function for sympy
sZ = 3*(1-sx)**2 * sym.exp(-(sx**2) - (sy+1)**2) \
	- 10*(sx/5 - sx**3 - sy**5) * sym.exp(-sx**2-sy**2) \
	- 1/3*sym.exp(-(sx+1)**2 - sy**2)

# create functions from the sympy-computed derivatives
# lambdify create function who is callable without sympy
# partial derivative of x
df_x = sym.lambdify( (sx,sy),sym.diff(sZ,sx),'sympy' )
# partial derivative of y
df_y = sym.lambdify( (sx,sy),sym.diff(sZ,sy),'sympy' )

# example for compute partial derivative at point 1, 1
df_x(1,1).evalf()

# random starting point (uniform between -2 and +2)
localmin = np.random.rand(2)*4-2 # also try specifying coordinates
startpnt = localmin[:] # make a copy, not re-assign

# learning parameters
learning_rate = .01
training_epochs = 1000

# run through training
trajectory = np.zeros((training_epochs,2))

for i in range(training_epochs):
	grad = np.array([ df_x(localmin[0],localmin[1]).evalf(),
	df_y(localmin[0],localmin[1]).evalf()
	])
	localmin = localmin - learning_rate*grad # add _ or [:] to change a variable in-place
	trajectory[i,:] = localmin

print(localmin)
print(startpnt)

# let's have a look!
plt.imshow(Z,extent=[x[0],x[-1],y[0],y[-1]],vmin=-5,vmax=5,origin='lower')
plt.plot(startpnt[0],startpnt[1],'bs')
plt.plot(localmin[0],localmin[1],'ro')
plt.plot(trajectory[:,0],trajectory[:,1],'r')
plt.legend(['rnd start','local min'])
plt.colorbar()
plt.show()
```
> lambdify: This module provides convenient functions to transform SymPy expressions to lambda functions which can be used to calculate numerical values very fast.

