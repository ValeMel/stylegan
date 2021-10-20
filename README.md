# stylegan3
NVidia's StyleGan series of papers and models aim at generating synthetic images from real images with controled modifications.
It provides a ready to use set of networks to generate fake images and a set of high quality images.
Applications are in photo edition (photoshop like), domain translation (winter to summer, old to young, etc.) and video generation.
It is AI and ANN powered. The NN learns from a set of images (either faces, or fish, or beaches, or flowers, or beds, etc) over several days on multiple high-end GPUs. 
It can as well be used as a pre-trained model and not require all the training.



How this is achieved is all based on Generative Adversarial Networks --> GAN. Relying on game theory, this architecture enables to put in competition 2 players, each of which is a machine learning model. 1 model is a discriminator: it receives an image as input and its output is whether the input image is fake or real. The objective of this model is to be as accurate as possible in its discrimination of real and fake images.

The other player model is a generator. It is just specified the characteristics of the desired output and it produces it. Its objective is to produce an image as real-looking as possible and thus deceiving the discriminator.

The competition can be formalized in technical terms by a minimax game with a value function reflecting the binary cross-entropy and the sochasticity of the process.

On top of this GAN architecture, StyleGAN enabled to build an image as a hierarchical synthesis of various layers of details of an image. The point is to control the various aspects of the desired output image at various resolution levels. It was enabled by 

. disentanglement. Disentanglement was obtained among others through progressively growing GANs with finer resolution (from coarse features like pose, and overall color, to face shape, or hair, stubble, freckles) 

. start generation from a constant and not a random variable. Noise is introduced in StyleGAN* at other levels. 
. integrate the learning into a mapping network and inserting performing affine scaling and biasing of Adaptive Instance normalization on top at various levels and in each layer



# How to train NVidia's stylegan3 
PyTorch implementation of the NeurIPS 2021 paper


# How to run stylegan3

