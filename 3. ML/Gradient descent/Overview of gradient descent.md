**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #gradientdescent 

## Theory
How deep learning models **learn**:
- Guess a solution.
- Compute the error (mistakes).
- Learn from mistakes and modify the parameters.

So: we need a mathematical description of the error "landscape" of the problem, and we need a way to find the **minimum** of the landscape.

## Example
Function:
$$
f(x) = 3x^2-3x+4
$$
Derivative of function:
$$
\frac{df}{dx}=6x-3
$$
1. Initialize **random** guess of **minimum**.
2. Compute the **derivative** at guess min.
3. **Update** guess min is itself minus derivative scaled by [[Learning rate]].

Math calculus by hand:
$$
\frac{df}{dx}=6x-3
$$
$$
0 = 6x-3
$$
$$
6x = 3
$$
$$
x=.5
$$

## Potential problems

### Informations
- Gradient descent is guaranteed to go "downhill".
- It is not guaranteed to find the correct - or even the best - solution.
- Gradient descent can go wrong if parameters are not set right for the particular landscape.
- Error landscapes are impossible to visualize in more than 2 dimensions.
###  Local minima

#### Problems
The success of deep learning, in spite of the "problems" with gradient descent, remains a mystery.
It is possible that there are many good solutions (many equally good local minima). This interpretation is consistent with the **huge diversity of weights configurations** that **produce similar model performances**.
Another possibility is that there are a **few local minima in high dimensional space**. This interpretation is consistent with the complexity and absurd dimensionality of deep learning.

#### Resolutions
> when model performance is good, don't worry about the local minima.

**One possile resolution**: Re-train the model many times using different random weights (different starting locationson the loss landscape) and pick the model that does the best.
**Another possible solution**: Increase the dimensionality (complexity) of the model to have fewer local minima.
