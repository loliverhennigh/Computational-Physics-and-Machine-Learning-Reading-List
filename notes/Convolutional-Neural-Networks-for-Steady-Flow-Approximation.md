
# Convolutional Neural Networks for Steady Flow Approximation

In this paper the authors use neural networks to predict steady state fluid flow around objects. The neural network takes in the boundary conditions (represented as by the Signed Distance Function) and predicts the steady state velocity vector field around the boundary. They find that the network can generalize extremely well and after being trained on simple polygons is able to make accurate prediction of flow for vehicle cross sections. The speed ups they present are around 100x when comparing a GPU fluid solver to their network and 10000x when comparing to a CPU solver.

## Notes

- The idea of this paper is quite nice and I feel that a similar approach could be applied to a wide variety of physics simulations. For example, you could compute the stresses in an object given its geometry and some forces on it.

- This paper is somewhat old and the neural network architecture has not aged well. In the bellow implementation of the paper I use a fully convolutional network and find that better performance can be had. This paper also uses the signed distance function as input to the network. By using an all Conv network this seems to eliminate the need for this.

## Source Code

This source code is not from the original authors but it is a close approximation to the paper.

https://github.com/loliverhennigh/Steady-State-Flow-With-Neural-Nets



