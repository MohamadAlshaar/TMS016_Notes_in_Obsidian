A **non-linear filter** useful for removing "salt-and-pepper" noise:
$$
g(i, j) = \operatorname{median} \left\{ f(i + k, j + l) : -r \leq k, l \leq r \right\}
$$
where $k$ and $l$ are directions instructing how to move in grid (matrix), $k$ tells how to move vertically and $l$ is horizontally.