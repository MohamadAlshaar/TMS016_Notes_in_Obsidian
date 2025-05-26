
In contrast to random fields, example [[Markov Random Fields]], we can observe data as pints on graph. The data is no longer on a continuous surface, but rather a set of points/events. 

Example when observing a forest:
- In **random fields**, we measure how the height of a terrain changes everywhere (the level).

- Whilst in **point processes**, we look where the trees are, $i.e$ what value each location have.

**Good example of a point process: Poisson Distribution.**

To formulate a point process:
- Pick a field $S$
- Specify the space $N$ that is locally finite
- Make $X$ a random variable of $N$

	*Model your spatial statistics (the field) and then model you point process*



To be more specific, one can choose from the many [[Types of Processes]]. You use those to model the processes.

Just like in [[2 Model Dependencies and Kriging]], we talked about how we extracting information like mean and covariance help us see how the field behaves, similarly here, we have certain **[[Point Process Characteristics]]** like intensity (number of points at certain areas) and correlation pairs to extract information. These help you extract information to see how well you model/[[Types of Processes]] worked.

A point process can also be [[Stationary]] and [[Isotropy]], just have a different interpretation here.
Here, it is interpreted as:
- Stationarity:$$
X \sim X + t \quad \text{for any translation } t \in \mathbb{R}^d
$$
	Meaning intensity is constant and the **pairwise interaction** only depends on relative position, $i.e$, looks statistically the same everywhere.

- Isotropy:$$
X \sim R_\theta(X) \quad \text{for any rotation } R_\theta
$$
	Pairwise statistics depend only on the **distance** $∣s−t∣$,$i.e$, looks the same in all directions, just like an even forest.

- Motion invariants:
	When both stationary and isotropic.