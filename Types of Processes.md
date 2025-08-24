
To model your point process, we can use:

- **Temporal Point Process:**
		The whole domain $S$ is $1D$ time interval $[0,T]$, *example*- Poisson Processes, Phone calls...
			**Poisson Process:** No interaction. Events are independent and scattered. Can be homogeneous (constant intensity) or inhomogeneous (spatially varying intensity) 

- **Spatio Temporal Point Process:**
		Domain is $S=T\times W$, $i.e$ we want to observe time and location.

- **Marked Point Process:**
		Each event $x_i$ is augmented by a mark $m_i$ such that we have $(x_i, m_i)$, meaning it has an attribute, *example*- a tree and its size. Marks can be dependent or independent on a location.

- **Cox Process:**
		Where it can be spatial, temporal, spatio-temporal or other. The difference is, this one is stochastic (random)- meaning the intensity function itself is random. 
  
- **Gibbs/Markov Process**:
		Interactions between points are explicitly modelled via an **energy function**. To create repulsion (increase) or inhibition (decrease), *if two points are too close, penalize them (repulsion), and vice versa (inhibition)*.
			**Strauss Process**: is a specific type of this, it models repulsion between nearby points, *example*- trees that need space between them, this process penalizes *trees* that are too close.


See [[Point Process Characteristics]] to understand intensity.