**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #gradientdescent 

# Vanishing gradient
Vanishing gradient problem is caused when derivative is near to 0 (when curve of gradient descent is flat), who make steps to tiny.
- Weights don't change -> no learning.

# Exploding gradient
Exploding gradient problem is when curve is too steep, nexts step in gradient descent are going really large, and local minimum is missed.
- Weights change wildly -> bad solutions.

# Minimize gradient descent problems
- Use models with few hiddent layers.
- Use activation functions that do not saturate (e.g., ReLU).
- Apply weight normalization.
- Pre-train networks using autoencoders.
- Use regularization techniques like batch normalization, dropout, and weight decay.
- Use architectures like residual networks ("resnet").