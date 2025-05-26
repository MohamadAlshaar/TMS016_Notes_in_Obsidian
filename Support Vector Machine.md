
Just like a linear regression model. SVM is a generalisation of linear discrimination (e.g., LDA in [[Discriminant Analysis]]), which instead of modelling distributions or relying on neighbours (like[[M-Nearest Neighbours]] ), it **finds the optimal separating hyperplane** between classes, *example*- we want to separate dogs from cats by a line (or planes in higher dimensions) and say everything on this side of the line is dogs and the other side is cats.

The model/decision function is:
$$
f(x) = \beta_0 + x^T \beta
$$Literally a linear model, if that equation is $=0$ then we are at the line, so we look at positive or negative values to see what side we are on, $a.k.a$ cats or dogs.

From our line, we can **support** it by adding a line on each side with a certain distance, formally called a **margin:** $M=1/||(\beta)||$, we want to maximize this margin since the further away the classes are from our line the better and more accurate the classification is. 

In practical situations, we add a **soft margin** that allows some misclassifications or violations in order to still find a good separating hyperplane when the data is not perfectly linearly separable, meaning *allow some dogs to be between cats and some cats between dogs for the greater good of the estimation*. Each misplaced class in this margin has a distance $\epsilon \geq 0$ (which is a slack variable for optimization problems) from the point to our our line, and we can add them all together and add a penalty if it gets too large:$$
\min_{\beta, \beta_0, \xi} \quad \frac{1}{2} \|\beta\|^2 + C \sum_{i=1}^{n} \xi_i
$$subject to:

$$
y_i(\beta^T x_i + \beta_0) \geq 1 - \xi_i, \quad \xi_i \geq 0
$$
(This becomes an optimization problem)



As we said, in higher dimensions, instead of using lines to separate classes we can use kernel functions, most common ones:
- Linear kernel: $K(x, x') = x^T x'$
- Radial basis kernel: $K(x, x') = \exp\left( -\frac{\|x - x'\|^2}{2\sigma^2} \right)$
- Polynomial kernel: $K(x, x') = (x^T x' + c)^d$

Kernels can also be used to move up (or down) in dimensions to better separate the classes ,example, You can’t separate them with a line in $2D$.  But if you map a sphere now your data lies along a new axis — the radius — and becomes **linearly separable** in this **1D radial space**. 