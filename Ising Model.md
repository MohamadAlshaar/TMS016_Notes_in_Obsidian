A way to control behaviour of [[Markov Random Fields]].
<<<<<<< HEAD
Sets a boundary condition on the matrix/domain and tell pixels how to be matching within this boundary, big parameter $\beta \rightarrow$ Big match and vice versa . This boundary conditions is either $[0,1]$ or $[-1,1]$ where $-1$ indicate down-spins and 1 are up-spins. 
=======
Sets a boundary condition on the matrix/domain and tell pixels how to be matching within this boundary, big parameter $\beta \rightarrow$ Big match and vice versa . This boundary conditions is either $[0,1]$ or $[-1,1]$ where $-1$ indicate down-spins and 1 are up-spins. In other words $x_s \in \{-1, 1\}$ (Binary).
<<<<<<< HEAD
>>>>>>> d4794ce (update)
There is a transition point for $\beta$ (think Bifurcation Point) where if:
	$\beta > \beta_c$  : Long range dependencies where we either have more up-spins than down, or vice versa.
	$\beta < \beta_c$  : No phase transition, meaning up-spins $=$ down-spins, or in other words, pixel values are $\approx 0$ in large areas. 
=======
There is a transition point for $\beta$ (think Bifurcation Point) where if for $\beta_c= \ln(1+\sqrt2)/2 \approx 0.44$   :
	$\beta < \beta_c$  : Long range dependencies where we either have more up-spins than down, or vice versa.
	$\beta > \beta_c$  : No phase transition, meaning up-spins $=$ down-spins, or in other words, large patches of white or black. 
>>>>>>> 64c15b1 (Uppdaterade)
	$$
P(X = x) = \frac{1}{Z} \exp\left( \beta \sum_{\{s, s'\} : s \leftrightarrow s'} x_s x_{s'} \right)
<<<<<<< HEAD
$$
=======
$$
Obviously we want the output to be binary too, so $Z$ here acts as a normalizing function (so called partition function).
>>>>>>> d4794ce (update)
