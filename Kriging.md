Kriging gives the **best linear unbiased prediction of $X(s_0​)$ given the observed values.

We have:
- Observations: $x(s_1) \dots x(s_n)$ 
- Locations: $s_1 \dots s_n$

We want:
	*Predict the value of $X(s_0)$ at some new location $s_0$*
	
**Formally:**
For the Gaussian field:

$$
\begin{pmatrix}
X_1 \\
X_2
\end{pmatrix}
=
\begin{pmatrix}
X(s_1), \ldots, X(s_n) \\
X(s_0)
\end{pmatrix}
\sim \mathcal{N} \left(
\begin{pmatrix}
\mu_1 \\
\mu_2
\end{pmatrix},
\begin{pmatrix}
\Sigma_{11} & \Sigma_{12} \\
\Sigma_{21} & \Sigma_{22}
\end{pmatrix}
\right)
$$

Where $\sum$ is the [[Covariance Matrix]]. 
Then the **conditional distribution** $i.e$ the **Kriging Predictor** is:

$$
X(s_0) \mid X(s_1), \ldots, X(s_n) \sim \mathcal{N} \left(
\mu_2 + \Sigma_{21} \Sigma_{11}^{-1} (X_1 - \mu_1),
\Sigma_{22} - \Sigma_{21} \Sigma_{11}^{-1} \Sigma_{12}
\right)
$$
Or simply, the **Kriging Predictor**:
$$
\hat{X}(s_0) = \mu(s_0) + \mathbf{c}^T \mathbf{\Sigma}^{-1} (X_1 - \mu_1)
$$
See [[Solve Matrix]].


#### Steps to apply:

- Formulate the model (you need a relationship between input and output):$$
Y_i = \sum_{k=1}^{K} B_k(s_i) \beta_k + X(s_i) + \varepsilon_i
	$$
	- $B_k(s)$ are covariates (known functions, something you know at all locations, yani some pattern) 
	- $\beta_k$ unknown coefficient for the covariates (how they change)
	- $X(s_i)$ is the random variable in your field
	- $\epsilon$ is the error


- Use the **Kriging Predictor** at each unknown location, example:$$
\hat{X}(s_0) = \mathbb{E}[X(s_0) \mid X(s_1), \ldots, X(s_n)]
$$for the full model

$$
\hat{Y}(s_0) = \sum_{k=1}^{K} B_k(s_0) \hat{\beta}_k + \hat{X}(s_0)
$$


**Note**
One can use Maximum Likelihood to estimate the parameters, trade off? more bias since you lose $n-p$ degrees of freedom.


**Different types of Kriging:**

- **Simple Kriging**: 
	 where  $\mu(s) = B(s)\beta$ is known. You know the mean of the field at each location.

- **Ordinary Kriging**:
	 where $\mu(s) = \beta$ is unknown but constant. You assume a flat mean across the grid and estimate $\beta$ from the data

- **Universal Kriging**: 
	 where $\mu(s) = B(s)\beta$  is unknown. You model it using known covariates $B(s)$.