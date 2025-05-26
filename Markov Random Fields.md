"We want to create structure and spatial dependencies in the image between pixels, we say each pixel is dependent on its neighbour"
- Properties:
	- A pixels $S$ is not neighbour of it self
	- Symmetry: *"if you are my neighbour, I'm your neighbour"*


**Can be either in Discrete and Continuous:**

**Discrete MRF**:
	The random variable $X_s$​ takes values from a **finite or countable set**.
	Example: **[[Ising Model]]**
	Used in: Binary Images and Image segmentation


**Continuous MRF**:
	The random variable $X_s$​ takes real values.
	Example: [[Auto-normal MRF]]
	Used in Greyscale Images and Geostatistics
	Usually Gaussian Distribution,


**Problem?**
The normalizing constant $Z$ in the density functions in the models often are too large and unknown. Therefore we use [[Markov Chain Monte Carlo Methods]].
