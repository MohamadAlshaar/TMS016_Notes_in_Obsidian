
Already know!
Input an image, pass it through multiple layers (linear + non-linear) ,to model the probability the and image $X$ belongs to a class $\omega_k$. The output is compared to the true label, and the **error** is used to update the weights via  **Backpropagation** to update your weights. 

If we notice that the NN performs well on training data but poorly on new data, we call it **Overfitting**.

To fix overfitting:
- Stop updating the weights (validating the error) when it is low enough
- **Regulation**:
		Add penalty to big wights in the loss, why? well since big wights are what influence the NN the most.  (Loss here is **cross-entropy loss**, tells us how confident the model is)

A popular NN in Computer Vision is CNN, [[Convolutional Neural Network]].