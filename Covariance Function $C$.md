Valid if:
- $C$ is symmetric $i.e$ if $c(s,t)=(t,s)$
- C is positive semi-definite : $\sum_{i=1}^{n} \sum_{j=1}^{n} a_i a_j C(s_i, s_j) \geq 0$

	*To model how neighbouring pixels correlate to each other*.

When modelling **spatial data** (e.g. temperature maps, terrain, grayscale images), we want to define the **covariance structure** of the field $X(s)$. That is, how values at different locations are correlated in the [[Joint Distribution]]. 

In practice we also say that the field is either [[Stationary]] or [[Isotropy]] to use statistical properties to model $C$. 


