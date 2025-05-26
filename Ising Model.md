A way to control behaviour of [[Markov Random Fields]].
Sets a boundary condition on the matrix/domain and tell pixels how to be matching within this boundary, big parameter $\beta \rightarrow$ Big match and vice versa . This boundary conditions is either $[0,1]$ or $[-1,1]$ where $-1$ indicate down-spins and 1 are up-spins. 
There is a transition point for $\beta$ (think Bifurcation Point) where if:
	$\beta > \beta_c$  : Long range dependencies where we either have more up-spins than down, or vice versa.
	$\beta < \beta_c$  : No phase transition, meaning up-spins $=$ down-spins, or in other words, pixel values are $\approx 0$ in large areas. 
	$$
P(X = x) = \frac{1}{Z} \exp\left( \beta \sum_{\{s, s'\} : s \leftrightarrow s'} x_s x_{s'} \right)
$$