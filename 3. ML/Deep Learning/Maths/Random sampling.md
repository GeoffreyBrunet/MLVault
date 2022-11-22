**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definition of sampling variability
Different samples from the same population can have different values of the same measurement.
**Implication of sampling variability**: A single measurement may be an unreliable estimate of a population parameter.
Averaging together many samples will approximate the true population mean (**Law of Large Numbers**).

### Sources of sampling variability
**Natural variation**: Often seen in biology (e.g., height, weight) and physics (e.g., earthquake magnitude, number of stars per galaxy).
**Measurement noise**: The sensors are imperfect (e.g., electrical line noise, measuring µg with a gram-precision scale).
**Complex systems**: Measuring some factors while ignoring others (e.g., measuring height while ignorance age).
**Stochasticity (randomness)**: The universe is a wild and unpredictable place (e.g., photons hitting a camera lens).

# Why sampling variability is important in DL
- DL models learn by examples.
- Non-random sampling can introduce systematic biases in DL models.
- Non-representative sampling causes overfitting and limits generalizability.

# Code examples
## Numpy example
```python
import numpy as np

# create a list of numbers to compute the mean and variance of
x = [1,2,4,6,5,4,0,-4,5,-2,6,10,-9,1,3,-6]
n = len(x)
  
# compute the population mean
popmean = np.mean(x)

# compute a sample mean
sample = np.random.choice(x,size=5,replace=True)
sampmean = np.mean(sample)
```