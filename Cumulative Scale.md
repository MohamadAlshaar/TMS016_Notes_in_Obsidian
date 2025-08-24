
To capture a domains behaviour, especially $n\geq 2$

- **K-functions**: for second order interactions:
	Pick a random point, count how many other points are expected within radius $r$.
	In CSR (Complete spatial randomness):
$$
K(r) = \pi r^2
$$
	If $K(r) > \pi r^2$: clustering 
	if $K(r) < \pi r^2$: inhibition/repulsion
	 *''How many neighbors are within radius r on average?”

- **L-functions**: for second order interaction:
	Rescaling of $K(r)$ for easier interpretation.$$
	L(r)= \sqrt{K(r)/\pi}$$
	*“Given that many neighbors, what radius would you expect under CSR?”


- **Empty space functions:** for higher order interactions:
  Pick a random location in the study area. $F(r)$ is the probability there is a point within distance $r$:$$
F(r) = P(\text{distance from a random location to nearest point} \le r)
$$

- **Nearest neighbour distance distributions**: for higher order interactions:
  Pick a random point from the process. $G(r)$ is the probability its nearest neighbour lies within distance $r$:
$$
G(r) = P(\text{nearest neighbour distance} \le r)
$$
- Rises faster than Poisson if clustered.
- Rises slower than Poisson if regular.

- **J-functions**: for higher order interactions:
	Compares _nearest-neighbour distances_ $(G)$ with _empty-space distances_ $(F)$.
	$$
J(r) = \frac{1 - G(r)}{1 - F(r)}
$$
    
- J$(r)<1$: clustering.
    
- $J(r)>1$: inhibition.



