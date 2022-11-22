**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #maths 

# Definition of entropy in information theory
Entropy (defined by [Claude Shannon](https://fr.wikipedia.org/wiki/Claude_Shannon)) is a measure, a quantity that describes the amount of surprise or uncertainty that we have about a specific variable. Entropy is maximal at probabilities of $0.5$. At this value, events are maximally uncertain or unpredictable. It's fullu certain and predictable at probabilities of $0$ or $1$.
![](https://upload.wikimedia.org/wikipedia/commons/d/da/Mplwp_shannon_entropy.svg)
High entropy means that the dataset has a lot of variability.
Low entropy means that most of the dataset repeat (and therefore are redundant).

# Entropy formula
Calculate [nats](https://en.wikipedia.org/wiki/Nat_(unit)) for entropy:
$$
H = -\sum_{x}\textcolor{brown}{p}(\textcolor{purple}{x})\log(\textcolor{brown}{p}(\textcolor{purple}{x}))
$$
Calculate bits (or [shannos](https://en.wikipedia.org/wiki/Shannon_(unit))) for entropy:
$$
H = -\sum^{n}_{i=1}\textcolor{brown}{p}(\textcolor{purple}{x}_i)\log2(\textcolor{brown}{p}(\textcolor{purple}{x}_i))
$$
Where:
- $\textcolor{purple}{x}$ = data values
- $\textcolor{brown}{p}$ = probability
- $H$ = entropy
So we multiply the probability that an event occurs by the `log2` of that same probability for all the different possible events. Minus before sum is for get a positive number.

# Entropy VS variance
> Both are two different measures of variability.

- Entropy is non-linear and makes no assumptions about the distribution.
- [[Variance]] depends on the validity of the mean and therefore is appropriate for roughly normal data.

# Code examples
## Numpy example
```python
x = [0.25, 0.75]

H = 0
for p in x:
	H -= p*np.log(p)
```

