**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #gradientdescent 

## Python implementation
```python
import numpy as np
import matplotlib.pyplot as plt

# function
def fx(x):
	return 3*x**2 - 3*x + 4

# derivative
def deriv(x):
	return 6*x - 3

# plot the function and it's derivative
# define a range for x
x = np.linspace(-2, 2, 2001)
# plotting
plt.plot(x, fx(x), x, deriv(x))
plt.xlim(x[[0, -1]])
plt.grid()
plt.xlabel('x')
plt.ylabel('f(x)')
plt.legend(['y', 'dy'])
plt.show()

# random starting point
localmin = np.random.choice(x, 1)
print(localmin)

# learning parameters
learning_rate = .001
training_epochs = 1000

# run trough the training
modelparams = np.zeros((training_epochs, 2))
for i in range(training_epochs):
	# compute the gradient: the derivative of the local minimum
	grad = deriv(localmin)
	# redefine the local
	localmin = localmin - learning_rate * grad
	# store the value of local minimum and it's gradient at every single epoch
	modelparams[i, :] = localmin, grad

print(localmin)

# plot the results
plt.plot(x, fx(x), x, deriv(x))
plt.plot(localmin, deriv(localmin), 'ro')
plt.plot(localmin, fx(localmin), 'ro')
plt.xlim(x[[0, -1]])
plt.grid()
plt.xlabel('x')
plt.ylabel('f(x)')
plt.legend(['Empirical local minimum %s' %localmin[0]])
plt.show()
```