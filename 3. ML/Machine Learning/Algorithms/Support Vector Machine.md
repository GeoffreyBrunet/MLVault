**MOC**:: [[3.1. ML MOC]]
**Tags**:: #ml #algorithms 

# About
SVM is one of the simplest and most elegant methods for classification problems. It is a supervised learning algorithm. Each object that we want to classify is represented by a point in an n-dimensional space, and the coordinates of this point are called features.

SVMs perform classifications by drawing a line called a hyperplane in a 2-dimensional area, or a plane in a 3-dimensional area. Each category is on one side of this hyperplane. SVMs try to find the best separation between its two categories, by maximizing the distance between two points. This distance is called the margin, and the points that are directly on this margin are called Supporting Vectors.

To find the hyperplane, SVMs need a training set or a set of points, with labels corresponding to the right categories. In the background, SVMs solve a Convex Optimization Problem that maximizes the margin with the constraint of putting each point of each category on the right side.

If the points cannot be separated by a hyperplane on a 2D plane, one must add to the existing data non-linear data to be able to find a hyperplane on a 3D plane. Finally, we have to convert back to its origin in 2 dimensions to observe the hyperplane. This technique is called the Kernel Trick, and allows us to perform these steps efficiently.
