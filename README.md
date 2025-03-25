# Customer Segmentation using DBSCAN Clustering

## Overview:
This project performs customer segmentation on an e-commerce dataset using DBSCAN (Density-Based Spatial Clustering of Applications with Noise). The dataset contains customer purchase behaviors, including product categories, purchase frequency, and ratings.
The goal is to identify customer segments based on purchasing patterns and improve targeted marketing strategies.

## Features:
Data Preprocessing: One-hot encoding for categorical features and standardization of numerical features.
Dimensionality Reduction: Uses UMAP (Uniform Manifold Approximation and Projection) for feature transformation.
Clustering: Applies DBSCAN to identify customer segments.
Evaluation Metrics: Calculates Silhouette Score, Calinski-Harabasz Index, and Davies-Bouldin Index for cluster validation.
Visualization: Generates scatter plots to visualize clusters.

## Dataset:
The dataset contains customer transaction data with the following key features:

## Categorical Features: 
Country, Seasonal Occasion, Product Category

## Numerical Features: 
Purchase Frequency, Rating

## Installation:
To run the project, install the required dependencies:

pip install -r requirements.txt

Alternatively, install individual libraries:

pip install pandas scikit-learn umap-learn seaborn matplotlib

## Usage:
Run the clustering pipeline:

python main.py

This will:
Load and preprocess the dataset.
Apply UMAP for dimensionality reduction.
Perform DBSCAN clustering.
Save the clustered data.
Visualize the clusters.

## Methodology:
Data Preprocessing
One-hot encoding applied to categorical variables (Country, Seasonal_Occasion, Product_Category).
Standardization of numerical features (Purchase_Frequency, Rating).
Dimensionality Reduction:
UMAP is used to reduce the dataset to two components for better clustering and visualization.
DBSCAN Clustering:
Optimized hyperparameters: eps=0.33, min_samples=22.
Noise points are filtered out.
Cluster assignments are saved to the dataset.

## Evaluation:

### Silhouette Score: 0.96 (higher means better-defined clusters)
### Calinski-Harabasz Index: 201746.53 (higher indicates better separation)
### Davies-Bouldin Index: 0.05 (lower means better clustering)

## Results:
The clustering identified 15 customer segments, each representing different purchasing patterns.
Sample clusters:

Cluster	Size	Most Common Product Category	Avg. Purchase Frequency	Avg. Rating
0	45	Bandhanwars	5.27	3.81
1	37	Torans	6.05	3.94
2	23	Warli Art	5.70	3.96
...	...	...	...	...

## Visualization Example:

![DBSCAN Cluster Plot](image.png)

## Conclusion
The UMAP + DBSCAN combination effectively grouped customers based on their purchasing patterns.
The segmentation helps businesses target specific customer groups with personalized recommendations.
Future work could explore alternative clustering methods like HDBSCAN or K-Means for comparison.

## Contributor
Avaneesh1905

## License
This project is licensed under the MIT License.
