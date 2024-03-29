# Neural-Nets-From-Scratch
This notebook is a simple implementation of a neural net that provides functions to add and display neurons and connections and train the neural net on a training set. This notebook is intended to build an intuitive understanding of the neural net training process, and thus is optimized for readability rather than for performance. The training process was implemented using basic python libraries (though Networkx was used to graph the neural net). There is currently only support for Relu activation functions. 

My original intention for doing this was to build some intuition around neural nets, and perhaps gain a different perspective from deriving the process from first principles. Though neural nets still seem like a black box, I was able to clear out some of my misconceptions about the training process and  learn some greater takeaways about the Neural Net training process: 

1.  Activations of nodes to the right of a connection depend on the nodes on the left of a connection. This implies that parameters on layers closer to the input layer have more indirect impacts on the gradient of the cost function than parameters on layers closer to the output layer.
1.  This dependence of right node activations to left node activations is also what would make calculating gradients using finite differences very inefficient. Perturbing the value of the cost function for each paramater to estimate the derivative with respect to each paramater will impact the value for all values downstream of the neuron. This is also what makes automatic differentiation a much more useful technique in computing the gradients. I initially wanted to experiment with using wacky, noncontinuous activation functions (i.e. some arbitray piece of code which maps numbers using a programmatic function rather than a mathematical function), but this ended up being too computationally intensive to implement. 
1.  Cost functions do not need to be convex even though gradient descent is being used. Training relies on [a large number of paramaters to "wiggle" the cost function value out of local minima](https://www.quora.com/Are-neural-nets-always-convex-with-respect-to-the-weights-And-if-not-how-does-gradient-descent-work-so-well). The more paramaters there are in a neural net, the less likely it is to get stuck on a point where the gradient writh respect to *all* paramaters is 0. This limits the practical applications of this notebook, as the lack of optimizations limits the size of the neural net (and in turn the number of paramaters). 

# Notebook Structure
Neural Net.ipynb contains all of the methods to visualize and train the neural net in the first cell. There is also some sample code in the second notebook cell where an example neural net is constructed and trained. 

# Dependencies
This project uses [Jupyter](https://jupyter.org) and Python3. You can run this project by starting [Jupyter Notebooks](https://docs.jupyter.org/en/latest/running.html).

# Contributing
If you find any way to improve the educational value of this project or to increase the neural net visualization, feel free to create a PR!

# Acknowledgements

This project was started during my Summer 1 '20 batch at the [Recurse Center](https://www.recurse.com). Thank you to everyone in the community for providing a supportive and encouraging space for such a diverse collection of programmers.

