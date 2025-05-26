
A field that is both Gaussian and Markov, example as a graph:
$$X_1 \rightarrow X_2 \rightarrow X_3$$
$i.e$ the **Conditional Dependency** applies here:
$$
X_1 \perp X_3 \mid X_2
$$
Saying that nodes $X_1$ and X_3 $are$ related (dependant) only if node $X_3$ is given, which makes sense because $X_1$ and $X_3$ are not directly connected.
Making it Gaussian but also due to neighbouring properties the Markov behaviour is exhibited here.