Noted $\sum$  and tells you how much nodes/variables/pixels correlate. 

$\sum^{-1} = Q$

Where $Q$ is the [[Precision Matrix]].

Example,  a [[Gaussian Markov Random Field]] graph:

$$X_1 \rightarrow X_2 \rightarrow X_3$$

Here:
- $Q_{13}=0$ since $X_1$ and $X_3$ are not directly connected. 
- $\sum_{13}$ could be zero or not since it will show indirect correlations
-
$i.e$ the **Conditional Dependency** applies here:
$$
X_1 \perp X_3 \mid X_2
$$

This is a very large matrix, causing [[Kriging]] to be expensive $i.e$ $\rightarrow O(N^3)$.
We can reduce it to $O(N)$ by enforcing the matrix to be a **Sparse**- most of the elements are $=0$, practically this means that we enforce independency between variables (since $0$). 
See [[Solve Matrix]]
