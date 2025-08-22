
The idea is that we instead of computing exact probabilities, we **simulate** samples from the distribution using **Markov chains** that converge to the desired distribution.
<<<<<<< HEAD

These methods include:
- **Gibbs Sampling**
- **Metropolis Hasting**
=======
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
	- Start with some current state (say, a spin configuration).
	    
	- Propose a _small random change_ (e.g. flip one spin).
	    
	- Compute how much more/less probable the new state is compared to the old one.
	    
	- Accept the move with a certain probability:
	    
	    - If the new state is _better_ (higher probability), almost always accept.
	        
	    - If it’s worse, maybe accept (to avoid getting stuck).
	        
	- Repeat many times.
	    
	
	 Intuition: it’s like a _random hill-climb with wiggle room_: you mostly go towards better configurations, but sometimes step down so you don’t get trapped.
>>>>>>> d4794ce (update)
