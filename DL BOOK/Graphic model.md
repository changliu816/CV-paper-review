#  Structured Probabilistic Models for Deep Learning
***
## 1) Using Graphs to describe Graphic model
### Directed Models
   ![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2010-52-04.png)
### Undirected Models
   1) Clique potential + Partition function  
   * Clique potential measure the affinity of variables, and this factors are constrained to be nonnegative.
   
   ![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2010-58-39.png)
   * Partition function is a normalize constant to make porbability distribution summing to 1.
   
   ![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2010-57-38.png)  ![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2010-58-06.png)
   
   2) Energy-Based Models (Boltzmann machine)
   * A convenient way to enfoce the unnormalized density function larger than 0. It can avoid the problem that clique function should be carefully chosed. Otherwise, the partition function might diverge when integration such that the Gibbs distribution does not exist.   ![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2010-58-57.png)
   
   3) Free energy
   ![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2010-59-15.png)

## 2) Sampling from Graphic Model
   1) ancestral sampling (only for Directed model)
   * Very Fast and convenient.
   * Does not support every conditional sampling operation. 
   2) Gibbs sampling (For undirected model)
 
## 3) Advantage of Structured modeling
* Reduce cost of representing probability distribution as well as learning and inference.
* This makes our models easier todevelop and debug. We can design, analyze, and evaluate learning algorithms andinference algorithms that are applicable to broad classes of graphs

## 4) Learning about dependency
* In the context of deep learning, the approach most commonly used to model these dependencies is to introduce several latent or“hidden” variables,h. The model can then **capture dependencies** between any pair of variables vi and vj **indirectly**, via direct dependencies between vi and h, anddirect dependencies between h and vj.
* **A ﬁxed structure** over visible and hidden variables can use **direct interactions** between visible and hidden units to impose **indirect interactions** between visible units.

## 5) Inference and Approximate Inference
*  Computing the marginal probability of a general graphical model is #P hard.
* In the context of deeplearning, this usually refers to **variational inference**, in which we **approximate the true distribution p(h | v) by seeking an approximate distribution q(h|v)** that is as close to the true one as possible. 

