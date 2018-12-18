# Tutorial

## Genratative model Category
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
