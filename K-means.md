
This is a way to segment the image to be able to give different stuff labels when the labels are unavailable. Works by dividing the points to clusters (groups of points that are close to each other, with each cluster/group having a centre) and each cluster gets a label since it tells us what is different in the image and how much they differ.

Assume:
- Each pixel has a value (or a value vector) $x_i$
- For greyscale images (see[[1 General background]]) they get dimension $d=1$ since the intensity is either $0$ or $1$
- For RGB, $d=3$ since we have $3$ colours.

The algorithm:
1. **Choose number of clusters** \( K \)

2. **Initialize** \( K \) centroids (randomly or determine somehow), a centre point for each cluster

3. **Assign each data point** (e.g., pixel) to the nearest centroid

4. **Update centroids** as the mean of the assigned points

5. Repeat steps 3–4 until convergence (no change in the distances from points to the centroids)

**Note**: those models work when we want to define $2$ classes, the reason we choose more than $2$ though for example in GMM or K-means is to tell the algorithm that the class might differ in size, shape, intensity and so on, *even though we have only Rice or Not, different rice will have somewhat different shapes and intensities depending on shadows.*

