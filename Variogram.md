The **semi-variogram** is defined as:

$$
\gamma(s, t) = \frac{1}{2} \operatorname{Var}(X(s) - X(t))
$$
Or (in relation to the [[Covariance Function $C$]]):$$\gamma(s,t)=\frac{1}{2}(C(s,s)+C(t,t)-2C(s,t))$$
For a **stationary and isotropic** field:

$$
\gamma(s, t) = \gamma(|s - t|) = \sigma^2 \left(1 - \rho(|s - t|)\right)
$$

So it's essentially:
	*A measure of **how different** two values are expected to be, based on the **distance between their locations**.*

In the graph, the lower the value the better.
To make it more practical we add a **Nugget effect** that overlook distances that are $= 0$, because *if the distance is zero then we are looking at the same pixel essentially!* Which is wrong.

Once we have the variogram we want to pick a function to match the shape of our data called **Isotropic Correlation Functions**:
- Linear: $$
\rho(r; \theta) = 
\begin{cases}
1 - \frac{r}{\theta}, & r < \theta \\
0, & \text{otherwise}
\end{cases}
$$
- Spherical:$$
\rho(r; \theta) = 
\begin{cases}
1 - \frac{3r}{2\theta} + \frac{1}{2} \left( \frac{r}{\theta} \right)^3, & r < \theta \\
0, & \text{otherwise}
\end{cases}
$$
- Exponential:
$$
\rho(r; \theta) = \exp\left(-\frac{r}{\theta}\right)
$$
- Gaussian: $$
\rho(r; \theta) = \exp\left(-\left(\frac{r}{\theta}\right)^2\right)
$$
Where $\theta$ is a **scale** saying: how quickly correlation drops with distance.

But the most flexible one is The Matérn Correlation Function:
$$
\rho(r; \nu, \theta) = \frac{2^{1 - \nu}}{\Gamma(\nu)} \left( \frac{r}{\theta} \right)^\nu K_\nu \left( \frac{r}{\theta} \right)
$$

An *Empirical Variogram* essentially does the same thing, being the original, however the data here are presented raw. The variogram and those different functions (linear, spherical....) are a way to fit this raw data on a graph, meaning we smooth it out. Formally you compute it directly from your observed field $X(s)$:

$$
\hat{\gamma}(h) = \frac{1}{2N(h)} \sum_{\|s_i - s_j\| \approx h} \left[ X(s_i) - X(s_j) \right]^2
$$
It's a scattered cloud of points that shows how variability grows with distance.

