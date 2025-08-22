
Image segmentation that works by looking at the intensity, Rice or Not. It is one of the **simplest unsupervised segmentation methods**.  
You segment an image by looking at the **[[Intensity Histogram]]** and choosing a **threshold** value to separate regions, if under a certain value -> classify.
Example: $$
\text{If } f_{ij} \leq T \Rightarrow \text{ class 0,} \quad \text{else } \Rightarrow \text{ class 1}
$$
A good method to use since its cheap but use only if the histogram is a *Bimodal*, meaning the peaks in the histogram are clear and you have $2$ of them. Otherwise it becomes hard to choose the threshold. 

