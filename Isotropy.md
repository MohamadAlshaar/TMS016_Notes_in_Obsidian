The spatial relationship doesn’t depend on **direction** — only on **distance** between points (Rotation).
	*How far apart the pixels are*

**Formally:**

$$
(X(R_\theta(s_1)), \ldots, X(R_\theta(s_n))) \sim (X(s_1), \ldots, X(s_n))
$$

Where $R_\theta$  is a rotation. This means the covariance and hence the [[Covariance Function $C$]] depends only on the **Euclidean distance**:

$$
C(s, t) = C(|s - t|) = \sigma^2 \rho(|s - t|)
$$

Note that Distance here is the distance between pixels on our grid.