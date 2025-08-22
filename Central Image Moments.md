
Defined as:$$
\mu_{pq} = \sum_{(i,j) \in A} (i - \bar{x})^p (j - \bar{y})^q f_{ij}
$$
Where $\bar{x}, \bar{y}$ are calculated from [[Raw Moments]], and $A$ is the area (set of pixels somewhere). The value of this tells us to remove the **effect of translation**, so you can compare object **shapes** regardless of where they appear in the image. $i.e$ transform the coordinates.

A more specific way to transform the coordinates is to use [[Hu Moments]], which takes rotation and resize into consideration when transforming.
