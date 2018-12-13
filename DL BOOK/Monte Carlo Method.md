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
