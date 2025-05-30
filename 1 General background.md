
The image is our mathematical domain/field, where $X$ ($i.e$ the random variable) are the pixels. 
	we have $n$ pixel, if pixels are IDD then we have noise. 


- Binary Images are where the pixels are Bernouli Distributed, $i.e$ they can either be Black or White.

- Grey level image is when pixel values are $[0,1)$, this interval is Normally Distributed.


**[[Markov Random Fields]]**
	*"We want to create structure and spatial dependencies in the image between pixels, we say each pixel is dependent on its neighbour"*
- Properties:
	- A pixels $S$ is not neighbour of it self
	- Symmetry: *"if you are my neighbour, I'm your neighbour"*

	To avoid biases in our models, we set **Boundary Conditions**- meaning we split the domain into many smaller domains and set boundaries on each, we can give those domains properties to control their behaviour, for example **Isotropy**- "Go in from a side, come out of the opposite side".
	
	We can control our spatial dependencies, $a.k.a$, how much we let each pixel want to match with its neighbours by using, for example, **[[Ising Model]]**- that is a Discrete MRF with certain behaviour, or **[[Auto-normal MRF]]**- that is a continuous MRF. 

	**Problem?**
	The normalizing constant $Z$ in the density functions in the models often are too large and unknown. Therefore we use [[Markov Chain Monte Carlo Methods]].


**Image Filtering**
	We can improve image properties by constructing a new image $g$ given an image $f$ by borrowing information from neighbours. This can be done as [[Linear filtering]] [[Median filtering]] or [[Gaussian filtering]]. 
	Filtering helps us in image segmentation and **[[Edge Detection]].** 