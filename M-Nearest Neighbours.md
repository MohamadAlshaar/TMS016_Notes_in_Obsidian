
In contrast to QDA and LDA in [[Discriminant Analysis]], here we **purely** rely on training data and distances between points. So **Not modelling densities at all**. 
Formally: “Non-parametric” means you **make no assumptions**, and **rely entirely on the raw training data** and distances for decision-making.

Suppose we have a training set $(x_i,y_i)$ where $y_i$ belongs to $K$ classes. For a new observation $x$, the neighbourhood $N_x$ is defined as the $M$ points ($M$ is neighbours) in the training set that are closest to $x$ (in a Euclidean sense).
Then, the **estimated probability** that $x$ belongs to class $m$ is:
$$
P(Y = m \mid X = x) = \frac{1}{M} \sum_{i \in N_x} I(Y_i = m), \quad m = 1, \ldots, K
$$
- $I(Y_i = m)$ is $=1$ if neighbour $i$ is of class $m$, and $=0$ otherwise

*Look at your M nearest neighbours. The class with the largest number of neighbours wins!*

