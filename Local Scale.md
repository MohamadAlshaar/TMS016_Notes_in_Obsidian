#### **Intensity Functions $\lambda (s)$**:
$$
\lambda(s) = \lim_{\Delta \to 0} \frac{\mathbb{E}[N(B(s, \Delta))]}{|B(s, \Delta)|}
$$

or simply $$
\Lambda(A) = \mathbb{E}[X(A)] = \int_A \lambda(x) \, dx, \quad A \subseteq S
$$
	This tells us the **expected Number of points per unit area** around location $s$, hence the intensity.
	*Places with high intensities tell us that near by places are expected to have similar intensity and so on*.
	$B$ here is a circular shape centred at a location $s$ with a certain  radius, to cover an area where wanna measure the intensity.
	**Note**: this can be done in higher dimensions as well.
	

#### Pair Correlation Function $g(s,t)$:

$$
g(x_1, x_2) = \frac{\lambda^{(2)}(x_1, x_2)}{\lambda(x_1)\lambda(x_2)}, \quad x_1, x_2 \in S
$$

- Cluster if $g(s,t)>1$
		The data are clustered together in different areas clumps.
- Completely Random if  $g(s,t)=1$
		Random behaviour, could be clustered somewhere and regular otherwhere and so on.
- Regular if $g(s,t)<1$
		Normally distributed data (I think)

	**So the function measures interaction between points: are they likely to appear close together or far apart**
	*How likely that $X$ has a point in $x_1$ and $x_2$*

