**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #parameter 

# About
Learnin rate is a small number that we use to make sure that we're taking small steps we don't miss the minimum.

## Possible ways to proportionate the learning rate
1. **Training epoch**: Good method, often done in blocks. But unrelated to model performance/accuracy. This method is called **learning rate decay**.
2. **Derivative**: Adaptive to the problem. Require additional parameters and appropriate scaling. This method is incorpoated into **RMSprop** and **Adam** optimizers.
3. **Loss**: Adaptive to the problem. Works only when loss is in range of \[0, 1\] (scaling possible).
4. **Current local minimum value**: Adaptive to the problem. Too many assumptions for this generally to be a good idea.