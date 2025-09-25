## Feature Reduction
## Dimensionality Reduction

- Principal Component Analysis (PCA)
	- Dimensionality Reduction
	- Visualization

- Steps for custom PCA
	- Perform Mean Centering
	- Find covariance matrix of features
	- Find Eigen values and Eigen vectors of covariance matrix
	- Sort Eigen vectors based on eigen values in descending order
	- Normaized eigen values is the explained variance
	- Project the vectors to Principal Components
	- Visualize the results, explined variance
	- Compare the results with library version

## T-SNE
- t-Distributed Stochastic Neighborhood Embedding
- Dimensionality reduction for visualization
- PCA tries to preserve global structure of data, but ignores local structures
- Neighborhood (points that are closer) and Embedding (finding representation in another low dimensional space)
- preserves distances of points in the neighborhood (not always e.g. Crowding problem)

## UMAP
- Uniform Manifold Approximation and Projection for Dimension Reduction (UMAP)