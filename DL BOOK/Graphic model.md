#  Structured Probabilistic Modelsfor Deep Learning
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
