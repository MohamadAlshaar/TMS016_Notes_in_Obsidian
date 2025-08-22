
We compute the probability of what we should expect, and then maximize it (**Bayes theorem**).

The **Expectation** step:
Compute the posterior probability that point $x_i$ belongs to a cluster $k$:
$$
r_{ik} = \frac{\pi_k \cdot \mathcal{N}(x_i \mid \mu_k, \Sigma_k)}{\sum_{j=1}^{K} \pi_j \cdot \mathcal{N}(x_i \mid \mu_j, \Sigma_j)}
$$
The **Maximization** step:
Update the parameters $\pi, \mu, \sum$ to maximize the likelihood

