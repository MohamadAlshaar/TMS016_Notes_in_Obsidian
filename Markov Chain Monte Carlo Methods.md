
The idea is that we instead of computing exact probabilities, we **simulate** samples from the distribution using **Markov chains** that converge to the desired distribution.
## The problem

Imagine you want to understand a very complicated probability distribution — like the Ising model, where the probability of a whole spin configuration depends on millions of tiny interactions.

- The distribution is too complex to compute directly (because of the huge partition function $Z$.
    
- But we’d really like to know what “typical” configurations look like, or estimate averages (mean spin, correlations, etc).
    

 So we need a way to **draw samples** from this complicated distribution without knowing $Z$.

These methods include:
- **Gibbs Sampling**:
	- If we have a complex probabilistic model, like the Ising model, that defines the probability distribution over the whole grid. What Gibbs does, since we don't know $Z$, we compute the conditional probability (probability given it's neighbor) of the spin (pixel-value $x_s \in \{-1, 1\}$) of each site ($a.k.a$ each pixel), then we update each site one at a time and when you have gone through all the sites in the grid we have done a full sweep and we now have a new grid-configuration. That grid-configuration is one sample, we repeat the process until we have many more samples (grid-configurations) to output a good approximation of the probabilistic model. 
	  To avoid biases, we get rid of the early iterations, since you start arbitrarily, the chain still **remembers** this starting point, so the first samples are biased- we call it burn in period.

	  Formally:
	1. Initiate by choosing a starting configuration $x^{(0)}$.
	
	2. For $i=1\dots n$:  
	   Generate 
	   $$
	   x^{(i)} = (x^{(i)}_1, \ldots, x^{(i)}_n)
	   $$
	   according to the following sequential updating:
	
	   - Draw site 1:
	     $$
	     x^{(i)}_1 \sim p(\cdot \mid x^{(i-1)}_2, \ldots, x^{(i-1)}_n)
	     $$
	   - Draw site 2:
	     $$
	     x^{(i)}_2 \sim p(\cdot \mid x^{(i)}_1, x^{(i-1)}_3, \ldots, x^{(i-1)}_n)
	     $$
	   - $\vdots$  
	   - Draw site n:
	     $$
	     x^{(i)}_n \sim p(\cdot \mid x^{(i)}_1, \ldots, x^{(i)}_{n-1})
	     $$
		When you have updated all sites once ($1$ through $n$), you have constructed a **new configuration of the whole grid**:  $x^{(i)} = (x^{(i)}_1, \ldots, x^{(i)}_n).$ Which was the goal.

	
- **Metropolis Hasting** 
	- We flip the spins to see how well the sites align with their neighbors.  In Gibbs, one sweep of the grid is one sample. Here, one site update is one sample.
	1. Initiate by choosing a starting configuration $x^{(0)}$. 
	2. Generate iterations $i \rightarrow i+1$
	   
		Pick a site $s$ at random.
		
		Propose a flip of spin.
		
		Compute energy difference.
		
		Compute acceptance probability.
		
		Accept or reject, if this new configuration is more probable accept, otherwise reject. 
		
	1. Repeat. 