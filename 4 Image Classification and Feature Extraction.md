

In [[2 Model Dependencies and Kriging]], we talked about how to filter data and model it, here we talk about how to label them and extract certain features, the difference here is that we want to define meaningful features and label them rather than just seeing how "covariance" and "mean" of the pixels behave. So this section is more about *Computer Vision*.


**Image Classification** is when we give labels to an image (or a part of an image/object), $example$, what is sky and what is water in an image. The core idea here is to use *Bayes Theorem* to guess what class the object has, $i.e$, find the posterior. 

We have $2$ classes, $\omega_1$ and $\omega_2$ and for each object (part of an image) observe a real valued feature- The goal here is to classify the object into either $\omega_1$ or $\omega_2$.  This is how we do it:

- **Prior Probabilities $\pi_1 , \pi_2$**: how likely is the object to belong to a class. *Example*- if we have more sky than water, we want $\rightarrow$ $\pi_{sky} > \pi_{water}$
- **Density Functions $f(x)_1, f(x)_2$**: describes distribution of the feature $X$ within the class. More density is what we look for 
- **Decision Regions $A_1, A_2$**: if in $A_1$ then not in $A_2$ 

All together we want to find: $$\pi_i f_i > \pi_j f_j$$
**Problem?** how do we find a proper **Density Functions**? 
For that we have the following classifying methods:
- [[Discriminant Analysis]] (Linear and Quadratic)

[[M-Nearest Neighbours]] is also a classifying method that doesn’t use Bayes’ rule directly, but can still get very close to its performance if you have enough data and a good distance metric.
#### However
We also want to reduce the [[Miscalculations]] and penalize them if we are wrong.


Other ways to classify an image using **machine learning**, specifically, [[Support Vector Machine]]. 

And in cases where we do not have labels to start with, we use **Image Segmentation** methods to decide labels, often to decide what is *background* or *not a background*, think of an image with a black background and rice on it, want to decide: rice or not. We use methods like:
- [[Intensity Based Thresholding]]
- [[K-means]]
- [[Gaussian Mixture Model]]
**Note**: those models work when we want to define $2$ classes, the reason we choose more than $2$ though for example in GMM or K-means is to tell the algorithm that the class might differ in size, shape, intensity and so on, *even though we have only Rice or Not, different rice will have somewhat different shapes and intensities depending on shadows.*

Up to now we have focused on how to label images, now we want to extract meaningful feature to be able to distinguish different classes. 

To extract certain features like shape and size, we use the [[Raw Moments]] to describe these features. But in order to make sure that when we change position of these shapes, the model doesn't think its something new, that's why we use [[Central Image Moments]] and [[Hu Moments]] to make the shapes invariant to position changes, $i.e$, if we have a circle in a corner, and we change the position of it, we still we want it to be a circle. 

We usually use [[Neural Networks]] to teach the model what certain features should be labelled as. A popular NN is [[Convolutional Neural Network]].






