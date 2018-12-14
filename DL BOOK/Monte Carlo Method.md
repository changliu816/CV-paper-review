# Monte Carlo Method

## Sampling and Monte Carlo Methods
### Why sampling?
* Approximation of a costly but tractable sum(speedup the process) or intractable sum (partition function of an undirected model)
* Sampling itself. Train a model that can sample from the training distribution

### Monte carlo sampling
* The idea is to view the sum or integral as if it were an **expectation under some distribution** and to **approximate the expectation by a corresponding average**

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2013-35-54.png)

* We can approximatesby drawing n samples x(1), . . . , x(n) from p and then forming the empirical average.

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Screenshot%20from%202018-12-13%2013-40-37.png)

* THis approximatio is justifed by 1) **the law of large numbers**(if samples are i.i.d, then the avearge converges almost surely to the expected value) 2) **The central limit therem**(the distribution of the average converges to a normal distribution with mean=s, and variance = var/n)

## IMportance Sampling
* Don't know which part is probability p(x), which part is f(x). Fortunately, the form of the optimal choice q∗ can be derived easily. The optimal q∗ corresponds to what is called **optimal importance sampling**.


* Any choice of sampling distribution q is valid (in the sense of yielding thecorrect expected value), and q∗ is the optimal one (in the sense of yielding minimumvariance). Sampling from q∗ is usually infeasible, but other choices of q can be feasible while still reducing the variance somewhat.

* Biased importance sampling
## Markov Chain Monte Carlo Methods
*  sampling from an **energy-based model** to make sure no zero probability assigned to any state
* Formally, a Markov chain is deﬁned by a random state x and a transition distribution T(x'| x) specifying the probability that a random update will go to state x' if it starts in state x. Running the Markov chain means repeatedly updating the state x to a value x' sampled from T (x'| x)

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Selection_001.png)

* If there is a nonzero probability of transitioning from any state x to any other state x' for some power t, then **the Perron-Frobenius theorem** guarantees that **the largest eigenvalue is real and equal to 1**. Over time, we can see that all the eigenvalues are exponentiated. This process causes **all the eigenvalues that are not equal to 1 to decay to zero**. A is guaranteed to have only one eigenvector with eigenvalue 1. The process thus converges to a **stationary distribution**,sometimes also called the equilibrium distribution.

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Selection_002.png)

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Selection_003.png)

![](https://github.com/changliu816/CV-paper-review/blob/master/photo/Selection_004.png)

* To be a stationary point,**v must be an eigenvector with corresponding eigenvalue 1**. If we have chosen T correctly, then **the stationary distribution q will be equal to the distribution p** we wish to sample from

### Drawbacks
* They are identically distributed, but any two successive samples will be highly correlated with each other. 
* Another diﬃculty is that we do not know in advance how many steps the Markov chain must run before reaching its equilibrium distribution. This length of time is called the **mixing time**

## Gibbs Sampling



