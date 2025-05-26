
In both LDA and QDA in [[Discriminant Analysis]]. We assumed that each class $\omega_k$ has:
- A prior probability $\pi_k$
		**Estimated** as: $\hat{\pi}_k = \frac{n_k}{n}$, for $n_k$ number of samples in class $k$ and $n$ total samples

- A mean vector $\mu_k$
		**Estimated** as $\hat{\mu}_k = \frac{1}{n_k} \sum_{i : y_i = k} x_i$, for the feature vector $x_i$ and $y_i=k$ being the class label for that sample

- A covariance matrix $\sum$ 
		In QDA **Estimated** as: $\hat{\Sigma}_k = \frac{1}{n_k - 1} \sum_{i : y_i = k} (x_i - \hat{\mu}_k)(x_i - \hat{\mu}_k)^T$, computing the sample covariance for each class.
		In LDA **Estimated** as: $\hat{\Sigma} = \frac{1}{n - K} \sum_{k=1}^{K} \sum_{i : y_i = k} (x_i - \hat{\mu}_k)(x_i - \hat{\mu}_k)^T$, also called the *Pooled Covariance Matrix*, since it is the same for all classes.



