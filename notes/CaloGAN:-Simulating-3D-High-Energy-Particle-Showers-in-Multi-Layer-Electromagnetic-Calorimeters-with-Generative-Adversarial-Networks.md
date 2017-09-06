
# CaloGAN: Simulating 3D High Energy Particle Showers in Multi-Layer Electromagnetic Calorimeters with Generative Adversarial Networks

(Too Long to Read) This paper looks at using a generative adversarial network to model particle showers inside calorimeters. The generator network produces 3 images corresponding to the 3 calorimeter detectors. The network was trained to take in both a latent space vector z and the desired energy and predict the detector readings. The discriminator tries to both tell if the readings are generator or not and how much energy is in them. Adding this energy to the loss makes the network easier to train as seen in other work ([auxillary GANs](https://arxiv.org/abs/1610.09585)). They report the generator network is 1000 times faster then the simulation code.


## Notes

- Not fully comfortable with the source material but the results seem quite good. 

- Trained on 16 k80 gpus. Damn I wish I had more GPUs...

