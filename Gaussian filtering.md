A **specific linear filter** using a Gaussian-shaped kernel for **blurring** the image smoothly:
$$
h(k, l) = \frac{1}{2\pi\sigma^2} \exp\left( -\frac{k^2 + l^2}{2\sigma^2} \right)
$$
where $k$ and $l$ are directions instructing how to move in grid (matrix), $k$ tells how to move vertically and $l$ is horizontally.
