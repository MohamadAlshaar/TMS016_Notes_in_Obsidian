You apply a **kernel** (small matrix) over the image, computing a **weighted average** of each pixel and its neighbours:
$$
g(i, j) = \sum_{k=-r}^{r} \sum_{l=-r}^{r} h(k, l) \cdot f(i - k, j - l)
$$
where $k$ and $l$ are directions instructing how to move in grid (matrix), $k$ tells how to move vertically and $l$ is horizontally.

