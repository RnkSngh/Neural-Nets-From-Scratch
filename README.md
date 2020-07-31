# Neural-Nets-From-Scratch
This notebook is a simple implementation a neural net that provides functions to add neurons and connections, train the neural net, and display neuron activations and connections. This notebook is intended to illustrate the core training process, so the training was implemented using basic python libraries (though Networkx was used to graph the neural net). There is currently only support for Relu activation functions. 

My original intention for doing this was to build some intuion and bring a diverse perspective to the machine learning community. Though they are still a black box, I was able to clear out some misconceptions about the training process, I was able to learn some greater takeaways: 

1. The activations between left nodes
1. Coming from a bit of a numerical modeling background, I initially wanted to experiment with different activation fuinctions. It is numerically infeasible to compute gradients numerically (and it becomes
1.  This oen is explained both rigourously and nonrigourously (but intuitively): Cost functions are not always convex (for the non-math folks out there, that means finding where the gradients are zero only gaurantees that you have found a *local* minima rather than a gloabl one - i.e. you. 

But then how can you apply gradient descent to this then? The answer lies in the fact that you rely on. The chance of having the local minima with all paramaters zero decrease with the more number of paramaters. This is kind of the problem with implementing this very simple neural net - it certainly isn't optimized so it isn't the greatest at computing very large nets, but the non-convexity also makes it 


1. This one is more interesting than useful - itss totally not practical to think of Neural nets as computers, though they can be used to approximate any function. This means taht any tyope of computation can be used - i.e. any computer can be modeled by a gradietn descent problem? this really only provides a more complicated way of thinking about computation (would you rather visualize a simple set of or an n-dimensional function)? But it is interesting to drawing a connection between different types of communication. 

## Code Structure
This was implented by having a main class (i.e. the Neural Net) which stores all neurons on a layer into an array. Layers are in turn stored in an array. The connectivity between neurons is partially encoded in this array, and also throug 

