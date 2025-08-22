A type of NN, good for computer vision since we have a lot of variables/pixels, that a normal NN can not handle computationally.


Instead of treating the image as a flat vector, we look at local patterns. Convolution means *we scan the image and filter it*.

Imagine the input as a cube with many components, the second phase is to to filter it, split into smaller cubes with smaller components (each one presenting a certain feature). Third phase is to output a feature map (your features are now belonging and grouped in different maps).
When you get the output (Feature maps), flatten them and send it through a NN. 

Concepts like **Pooling** here are used to decrease the cost of the feature map, this means that instead of taking the value of each component in the map, take the average value of it. 



