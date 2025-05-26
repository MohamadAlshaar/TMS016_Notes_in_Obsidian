
Formally and generally:$$
m_{pq} = \sum_{(i,j) \in A} i^p j^q f_{ij}
$$
Saying *Combine the pixel intensities $f_{ij}$ with their positions $i,j$ and raise them to the powers $p,q$ (integers to manipulate depending on if we want mass, area, length etc)to get a summary of the shape*

We need **centroids** to figure out shapes and sizes, a centroid is just a way to define the central pixel that we want to observe and look around it (just a reference point), centroids are computed in coordinates of $x$ and $y$:
$$
\bar{x} = \frac{m_{10}}{m_{00}}, \quad \bar{y} = \frac{m_{01}}{m_{00}}
$$

Examples on how to compute shapes or sizes:
- Area can be calculated as the number of pixels in a shape.
- Perimeter, at the $8$ pixels surrounding the observed pixel, and if at least one of those $8$ pixels are not the same region, then we have an edge, and hence calculate the perimeter by adding those centroids.
- Width of shape: $max(x) -min(x)$
- Height of shape: $max(y) -min(y)$
- Shape compactness: $4\pi (|A|/P(A)^2)$
