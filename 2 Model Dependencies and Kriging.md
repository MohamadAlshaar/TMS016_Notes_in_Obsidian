
**Image Filtering**
	We can improve image properties by constructing a new image $g$ given an image $f$ by borrowing information from neighbours. This can be done as [[Linear filtering]] [[Median filtering]] or [[Gaussian filtering]]. 
	Filtering helps us in image segmentation and **[[Edge Detection]].** 


#### To **Model Spatial Dependencies,** we need the distribution, the covariance or some correlations:

We can extract a lot of information about the random variable $X$ (and the image) from its mean and covariance if it is a probabilistic [[Covariance Function $C$]]- that is valid if:
- $C$ is symmetric $i.e$ if $c(s,t)=(t,s)$
- C is positive semi-definite : $\sum_{i=1}^{n} \sum_{j=1}^{n} a_i a_j C(s_i, s_j) \geq 0$

The function is modelled according to the **[[Joint Distribution]]**.

But we can’t estimate a different covariance for every possible pair $(s,t)$ in $\mathbb{R}^2$ — that would be **too many parameters**!
So we make **simplifying assumptions** to reduce the complexity of the model, so we say that the field is either:
- [[Stationary]]
- [[Isotropy]]


#### **However**,
Because in practice, when working with **real spatial data**, it's often **much easier and more stable** to estimate a **[[Variogram]]** to figure out the **[[Covariance Matrix]]** and the [[Precision Matrix]] rather than a **covariance function**.

Once you have the covariance matrix $\sum$ , you can use it in your **[[Kriging]]** to predict unknown values on the grid.

