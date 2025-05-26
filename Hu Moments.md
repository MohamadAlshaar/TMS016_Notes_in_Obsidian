
As mentioned [[Central Image Moments]], a more accurate way to transform coordinates without affecting the shape or size, this methods take stuff lie:
- Translation
- Scaling 
- Rotation
Into consideration when transforming the coordinates. There are 8 central moments which are translation, rotation, or scale invariant, and they are called **Hu moments**

Start first by normalizing the Central moments:
$$
\eta_{pq} = \frac{\mu_{pq}}{\mu_{00}^{1 + \frac{p + q}{2}}}
$$
Which are the scale invariants, and then combine them into $7$ moments invariants:$$
\phi_1 = \eta_{20} + \eta_{02}
$$

$$
\phi_2 = (\eta_{20} - \eta_{02})^2 + 4\eta_{11}^2
$$

$$
\phi_3 = (\eta_{30} - 3\eta_{12})^2 + (3\eta_{21} - \eta_{03})^2
$$

$$
\phi_4 = (\eta_{30} + \eta_{12})^2 + (\eta_{21} + \eta_{03})^2
$$
and so on up to  $\phi_7$ ....