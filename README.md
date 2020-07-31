# Neural-Nets-From-Scratch
This notebook is a simple implementation a neural net that provides functions to add neurons and connections, train the neural net, and display neuron activations and connections. This notebook is intended to illustrate the core training process, so the training was implemented using basic python libraries (though Networkx was used to graph the neural net). There is currently only support for Relu activation functions. 

My original intention for doing this was to build some intution around the black box, and build a deeper understanding. Though neural nets are still a black box to me, I was able to clear out some misconceptions about the training process and  learn some greater takeaways about the Neural Net training process: 

1. The activations of right nodes depend on left nodes. Therefore, the paramaters associated with connections towards the left can be seen as having more impacts (indirectly through the chain rule) than the paramaters associated with connections towarsd the right. This is because left nodes will impact the activation of right nodes. 
1.  I initially wanted to experiment with different activation fuinctions - what if we could describe random snippets of code to use our activatino functions? Though after actually trying to implement this, I realized that numerically calculating the gradient would mean estimating small changes in the function while perturbing the values from their positions each time, which can be very numerically intensive to do for each paramater. This highlights the importance for finding analytical simplifications for calculating the gradient, and thus limits use of activation functions to analytically differentiable functions. 
1.  Cost functions do not necessarily need to be convex even though gradient descent is being used. Training relies on a large degree of paramaters to "wiggle" the paramaters out of areas where there are local minima. 



