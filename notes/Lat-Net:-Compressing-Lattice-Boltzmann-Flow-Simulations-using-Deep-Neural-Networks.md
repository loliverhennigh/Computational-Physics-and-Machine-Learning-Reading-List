
# Lat-Net: Compressing Lattice Boltzmann Flow Simulations using Deep Neural Networks 

Disclaimer, My paper.

In this paper the authers apply Neural networks to emulating lattice boltzmann type physics simulations. The method works by compressing the state of the simulation and then learning the dynamics on this compressed state. For example, in 2d fluid simulations it takes the lattice state as a 2D image with depth 9 (for D2Q9 scheme) and compresses that onto a much smaller space. Then it applies a compression mapping network that emulates steps in the lattice boltzmann solver. Then to decompress the state it uses a decoder network. There is a speed up of around 10x and memory efficency gain of 3.4x if you just compare the compression mapping to the actuall steps in the lattice boltzmann solver. Both of these gains are lost when having to decompress the state though. The author justifies this by saying that every state of the simulation does not need to be decoded and when decoding only portions of the state can be extracted. The method presented works on other forms of lattice boltzmann simulations and the authors illustrate this on electromagnetic simulations.

## Notes

- This is my paper and its still kinda in rough draft mode. In the comming months I will add new results and improve the 3D simulations. In particular, my goal is to perform a simulation of size 1000x1000x2000 using a amazon XLarge GPU instance. A simulation of this size would normaly require a massive multi server super computer (Tokyo group did it with 200 GPU in 2014) because of the memory requirements. Making use of the compression techneuque, I should be able to do this with only 52 Gb of working memory where as a modern LB solver would require around 180 Gbs.

## Source Code

https://github.com/loliverhennigh/Phy-Net

