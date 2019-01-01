# Unsupervised Learning


## Why unsupervised Learning ? 
1. Targets / rewards can be difficult to obtain or define. **Labels data are far less** than unlabel data
2. Unsupervised learning feels more **human** (From cognitive perspective)
3. Want rapid **generalisation to new tasks** and situations

## Category
1) Clustering
2) Density estimation
3) Dimension reduction
4) Sparce coding/ Auto-encoder


### Method 1 -  Density Modelling
* Do maximum likelihood on the data to learn the True distribution
* Generative model of data
### Problem (Where to look?)
* **Complexity**: density modeling is hard ! TOo many information and complex interaction between variables (Curse of dimension)
* **Need attention on specifical structure**:  Not all bits are created equal. Eg. image, log-likelihood depend more on low-level details than on high level strcuture (semantics, img content.)
* **Make sure the learned hidden structured is useful for other tasks**  How to exploit the underlying structure for future tasks (representation learning)

### Model 2 Autoregressive Models (RNN)
* Simple to define, but expensive and slow. 

---
## Practical method
• Learning representations 
• Learning to generate samples (just a brief mention)
• Learning to map between two domains 

## Biggest challenges:
• metrics & tasks,
• generality and efficiency of current algorithms,
• integration of unsupervised learning with other learning
components. 
