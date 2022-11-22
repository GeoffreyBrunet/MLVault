**MOC**:: [[3.1. ML MOC]]
**Tags**:: #ml #algorithms 

# About
The k-nearest neighbor method is one of the simplest supervised learning methods that can be used for regression and classification cases.

To apply this method, the steps to follow are the following:
- We fix the number of neighbors k.
- We detect the k-nearest neighbors of the new input data we want to classify.
- We assign the corresponding classes by majority vote.

But, how do we choose this parameter k during the implementation of the algorithm?
- We vary k
- For each value of k, we calculate the error rate of the test set
- We keep the parameter k which minimizes this test error rate.
