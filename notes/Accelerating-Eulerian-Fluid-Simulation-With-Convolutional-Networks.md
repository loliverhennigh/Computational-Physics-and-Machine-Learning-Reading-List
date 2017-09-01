
# Accelerating Eulerian Fluid Simulation With Convolutional Networks

The authors apply Convolutional Neural Networks to solving the Poisson equation in the Pressure Projection step of Eulerian Fluid Flow. The basic idea is that when doing eulerian fluid simulation the majority of the computation is used to solve the poisson equation. By having a Neural Network solve this problem instead of something like PCG, a significant computation boost can be gained. A interesting aspect of this paper is the loss function. A neive approach would be to generate a set of fluid simulations and then train on them with the neural network. They demonstrate an alternative approach where the neural network actually just learns to minimize the divergence of the velocity vector field. This has the benifit of making the training process unsupervied and not needing a big set of training examples. They do require the simulation to be initialized with the flow solver though.

## Notes

- This is one of the best and most interesting ways to apply machine learning to CFD that I have seen. It combines the both flow solver and neural networks in a very elegant way. It is also easy to see how this method can be redially applied to a variety of other problems.

- As Noted, above the loss function is completely unsupervised. It is able to learn to solve the Poisson equation just by minimizing the divergence of the predicted velocity field. I am curious if this type of technieqe is possible with other kinds optimization problems. For example, the possion equation is convex and thus not too difficult to solve. Could you train a network to optimize something that is nonconvex with this form of unsupervised learning? In this [project](https://github.com/loliverhennigh/Steady-State-Flow-With-Neural-Nets/tree/boundary_learning) I attempted to do a simaler unsupervised techneque in predicting Steady State Flow. This proved to not work very well and I suspect that it was because the optimization I was trying to perform is highly non-convex.

## Source Code

https://github.com/google/FluidNet

## Two Minute Paper Video

https://www.youtube.com/watch?v=iOWamCtnwTc

