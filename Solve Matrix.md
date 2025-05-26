
In [[Kriging]] we want to compute the [[Covariance Matrix]]. 

We have the predictor:$$
\hat{X}(s_0) = \mu(s_0) + \mathbf{c}^T \mathbf{\Sigma}^{-1} (X_1 - \mu_1)
$$
Set: $X_1 - \mu_1= e$ giving us $e = \sum x^n$   


Use Cholesky:
$$\sum = L L^T$$
Such that:
- $L_\omega = e$ 
- $L^T x=\omega$
