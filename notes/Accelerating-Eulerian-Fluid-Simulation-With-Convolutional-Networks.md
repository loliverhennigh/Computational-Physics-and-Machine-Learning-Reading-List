
# Accelerating Eulerian Fluid Simulation With Convolutional Networks

The authors apply Convolutional Neural Networks to solving the Poisson equation in the Pressure Projection step of Eulerian Fluid Flow. The basic idea is that when doing eulerian fluid simulation the majority of the computation is used to solve the Poisson equation. By having a Neural Network solve this problem instead of something like PCG, a significant computation boost can be gained. A interesting aspect of this paper is the loss function. A naive approach would be to generate a set of fluid simulations and then train on them using Mean Squared Error or something similar. They demonstrate an alternative approach where the neural network actually learns to minimize the divergence of the velocity vector field. This has the benefit of making the training process unsupervised and not needing a set of pre-run simulations. They do require the simulation to be initialized with the flow solver though.

## Notes

- This is one of the best and most interesting ways to apply machine learning to CFD that I have seen. It combines both the flow solver and neural networks in a very elegant way. It is also easy to see how this method can be readily applied to a variety of other problems.

- As noted above, the loss function is completely unsupervised. It is able to learn to solve the Poisson equation just by minimizing the divergence of the predicted velocity field. I am curious if this type of technique is possible with other kinds optimization problems. For example, the Poisson equation is convex and thus not too difficult to solve. Could you train a network to optimize something that is non-convex with this form of unsupervised learning? In this [project](https://github.com/loliverhennigh/Steady-State-Flow-With-Neural-Nets/tree/boundary_learning) I attempted to do a similar unsupervised technique in predicting Steady State Flow. This proved to not work very well and I suspect that it was because the optimization I was trying to perform is highly non-convex.

## Source Code

https://github.com/google/FluidNet

## Two Minute Paper Video

https://www.youtube.com/watch?v=iOWamCtnwTc

