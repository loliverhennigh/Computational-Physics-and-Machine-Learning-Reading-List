
# Deep learning and the Schr¨odinger equation

In this paper the authors use a neural network to learn the mapping from a potential field to the ground-state energy of an electron in that potential. The network seems to be able to generalize quite well and predict fairly accurate energies even on random potentials. This method is also extendable to predicting kinetic energy and excited-state energy.

## Notes

- The paper mentions a Supplementary Information Section but the arxiv version does not have it. I am not sure how to get a hold of this.

- I would really like to see this tested on a 2 or more electron problem and then a very good comparison of run time for the solver and the network.

- 200,000 training examples were used. I found this a bit high and I wonder if this was really needed.

- This paper reminds me of when I had a network take in boundary conditions and predict the drag on the object.

## Source Code

None yet but this would a very easy and fun paper to reimplement. Probably take less then 3 days or so.

