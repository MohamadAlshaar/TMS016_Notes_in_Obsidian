
A DA is a **generative classifier** that tries to model **how the data was generated**, i.e., it models the **full probability distribution** of each class. This the major difference to the non-parametric classifier [[M-Nearest Neighbours]].


Assume we have:
- Classes $k\geq 2$ 
- Each object described as feature vector $X$
- Each class has a prior $\pi$ and density $f$

The discriminant could be analysed either linearly or quadratically depending on the feature vector $X$. The idea is to assign the vector to class with the highest score:
$$
\text{Assign } X \text{ to class } \omega_k \text{ if } g_k(X) = \max_j g_j(X)
$$
The *Covariance Structure* or the [[Covariance Matrix]] of the class distributions is what decides the complexity of the discriminant, either linear or quadratic.

#### Quadratic Discriminant Analysis:
- Each class $i=1,\dots k$ generates data from a multivariate gaussian distribution$$
X \mid \omega_k \sim \mathcal{N}(\mu_k, \Sigma_k)
$$
- Each class has its own [[Covariance Matrix]] (essentially what makes this quadratic)
- Giving us the QD function:$$
g_k(x) = -\frac{1}{2}(x - \mu_k)^T \Sigma_k^{-1}(x - \mu_k) - \frac{1}{2} \log |\Sigma_k| + \log \pi_k
$$


#### Linear Discriminant Analysis

- Also gaussian but:
$$
X \mid \omega_k \sim \mathcal{N}(\mu_k, \Sigma)
$$
- Meaning all the classes same the same [[Covariance Matrix]] (hence, simpler).
- Giving us the LD function:$$
g_k(x) = x^T \Sigma^{-1} \mu_k - \frac{1}{2} \mu_k^T \Sigma^{-1} \mu_k + \log \pi_k
$$


**In practice**, we also need a way estimate the parameters $\pi_i, \mu_i, C_i$. For that see [[Parameter Estimation]].