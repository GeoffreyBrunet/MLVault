**MOC**:: [[3. ML MOC]]
**Tags**:: #ml #theory
## Definition
As the name suggests, the input data is fed in the forward direction through the network. Each hidden layer accepts the input data, processes it as per the activation function and passes to the successive layer.

At each neuron in a hidden or output layer, the processing happens in two steps:
1.  **Preactivation:** it is a _weighted sum of inputs_ i.e. the _linear transformation of weights_ w.r.t to inputs available. Based on this _aggregated sum_ and _activation function_ the neuron makes a decision whether to pass this information further or not.
2.  **Activation:** the calculated weighted sum of inputs is passed to the activation function. An activation function is a mathematical function which adds non-linearity to the network. There are four commonly used and popular activation functions — sigmoid, hyperbolic tangent(tanh), ReLU and Softmax.
