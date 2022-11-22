**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #gradientdescent 

# Python code
```python
import numpy as np
import matplotlib.pyplot as plt

# the function
x = np.linspace(-2*np.pi,2*np.pi,401)
fx = np.sin(x) * np.exp(-x**2*.05)

# and its derivative
df = np.cos(x)*np.exp(-x**2*.05) + np.sin(x)*(-.1*x)*np.exp(-x**2*.05)
```
## Experiment 1: systematically varying the starting locations
```python
startlocs = np.linspace(-5,5,50)
finalres = np.zeros(len(startlocs))

# loop over starting points
for idx, localmin in enumerate(startlocs):
	# run through training
	for i in range(training_epochs):
		grad = deriv(localmin)
		localmin = localmin - learning_rate*grad
		# store the final guess
		finalres[idx] = localmin

# plot the results
plt.plot(startlocs,finalres,'s-')
plt.xlabel('Starting guess')
plt.ylabel('Final guess')
plt.show()
```

## Experiment 2: systematically varying the learning rate
```python
learningrates = np.linspace(1e-10,1e-1,50)
finalres = np.zeros(len(learningrates))

# loop over learning rates
for idx,learningRate in enumerate(learningrates):
	# force starting guess to 0
	localmin = 0
	
	# run through training
	for i in range(training_epochs):
		grad = deriv(localmin)
		localmin = localmin - learningRate*grad
		
		# store the final guess
		finalres[idx] = localmin

plt.plot(learningrates,finalres,'s-')

plt.xlabel('Learning rate')

plt.ylabel('Final guess')

plt.show()
```
