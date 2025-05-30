
In contrast to [[K-means]], GMM handles real world values better since it forms more of elliptic regions rather than the more circular ones in k-means. The idea here is that we assume that pixel values come from a mixture of several Gaussian distributions, one per class/segment. 
Formally:

$$
p(x) = \sum_{k=1}^{K} \pi_k \cdot \mathcal{N}(x \mid \mu_k, \Sigma_k)
$$

Where:

- $\pi_k$ : weight (prior probability) of cluster $k$ (sums to 1)  
- $\mu_k$ : mean of the $k$ -th Gaussian  
- $\Sigma_k$ : **covariance matrix** (shape/spread) of the Gaussian  
-  $\mathcal{N}(x \mid \mu_k, \Sigma_k$) : multivariate Gaussian density.

This will form a distribution curve with peaks, each peak is a class, since the density is high at those peaks. 
**Note**: those models work when we want to define $2$ classes, the reason we choose more than $2$ though for example in GMM or K-means is to tell the algorithm that the class might differ in size, shape, intensity and so on, *even though we have only Rice or Not, different rice will have somewhat different shapes and intensities depending on shadows.*

- GMM lets each cluster have its own **shape, size, and orientation**
    
- Each data point can **belong partially to multiple clusters** (soft membership)
    
- Better suited for data with **overlapping clusters**
#### However
To decide what pixel values should have for classes, we use the [[Expectation Maximization]] algorithm.