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

## How it works?
1) MinMax Game J_G = - J_D
2) NOn-saturating Game
In the minimax game, the generator minimizes the log-probability of the
discriminator being correct. In this game, the generator maximizes the log-
probability of the discriminator being mistaken.

3) Maximum likelihood game

We can think of D_KL (p|q) as preferring to place high probability everywhere that the data occurs, and D_KL(q||p) as preferring to place low probability wherever the data does not occur. From this point of view, the latter might yield more visally pleasing sampels, because the model will not choosing to generate unusual samples lying between modes of the data geerating distribution.


# Paper Read
## WGAN
1) Martin Arjovsky等人先阐述了朴素GAN因生成器梯度消失而训练失败的原因：他们认为，朴素GAN的目标函数在本质上可以等价于优化真实分布与生成分布的Jensen-Shannon散度。而根据Jensen-Shannon散度的特性，当两个分布间互不重叠时，其值会趋向于一个常数，这也就是梯度消失的原因。此外，Martin Arjovsky等人认为，当真实分布与生成分布是高维空间上的低维流形时，两者重叠部分的测度为0的概率为1，这也就是朴素GAN调参困难且训练容易失败的原因之一。 
2) 针对这种现象，Martin Arjovsky等人利用Wasserstein-1距离（又称Earth Mover距离）来替代朴素GAN所代表的Jensen-Shannon散度. 相较于Jensen-Shannon散度，Wasserstein-1距离的优点在于，即使pr,pg互不重叠，Wasserstein距离依旧可以清楚地反应出两个分布的距离。

## WGAN-Gradient penalty
WGAN-GP的贡献在于，它用正则化的形式表达了对判别器 D 的约束，也为后来GAN的正则化模型做了启示。此外WGAN-GP基本从理论和实验上解决了梯度消失的问题，并且具有强大的稳定性，几乎不需要调参，即在大多数网络框架下训练成功率极高。

## LSGAN

# Cycle_GAN (unpaired img2img translation)
* insert cycle transitivity to adv loss. Good for color, texture changes, not for geomoetric changes.

# Big GAN
