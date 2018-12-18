# Tutorial

## Genratative modelS 
1) Extractable explicit model (Fully visible belief network) PixelCNN
2) Explicit models requiring approximation.
* Variantional approximatios (VAE): The main drawback of variational
methods is that, when too weak of an approximate posterior distribution or
too weak of a prior distribution is used, even with a perfect optimization al-
gorithm and infinite training data, the gap between L and the true likelihood
can result in p model learning something other than the true

* Markov chain approximations (Bolzmann machine): can sometimes guarantee that x will eventually converge to a sample
from p model (x). Unfortunately, this convergence can be very slow, and there is
no clear way to test whether the chain has converged. 1)Presumably the underlying Markov chain approximation techniques have not scaled to problems like ImageNet generation.  2) compared to single-step generation methods, the multi-step Markov chain approach has higher computational cost

3) GAN
This is the key approximation technique
that sets GANs apart from variational autoencoders and Boltzmann machines.
Other deep generative models make approximations based on lower bounds or
Markov chains; GANs make approximations based on using supervised learning
to estimate a ratio of two densities.
