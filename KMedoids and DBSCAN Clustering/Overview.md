# Analysis of K-Medoids and DBSCAN Algorithms in Clustering  

In **unsupervised learning**, clustering algorithms are widely used to identify the optimal grouping of data. These approaches can be categorized into different families:  

- **Partitioning Approach**: K-Means, K-Medoids, etc.  
- **Hierarchical Approach**: DIANA, AGNES, etc.  
- **Density-Based Approach**: DBSCAN, OPTICS, etc.  
- **Grid-Based Approach**: STING, WaveCluster, etc.  

This notebook presents a **comparative analysis** between **K-Medoids** (Partitioning Approach) and **DBSCAN** (Density-Based Approach), focusing on which method is more effective at discovering the optimal number of clusters.  

## Datasets Used  
Three types of datasets with different structures were employed:  
- Blob  
- Moon  
- Circle  

## Parameter Selection  
- **K-Medoids**: Since the number of clusters (*k*) must be specified in advance, the **Elbow Method** and **Silhouette Score** were used to estimate the optimal value of *k*.  
- **DBSCAN**: The **k-distance graph** was applied to determine suitable values of **ε (epsilon)** and **MinPts (minimum points)**.  

## Key Insights  
- **K-Medoids** (centroid-based):  
  - Works well with spherical/compact clusters.  
  - Struggles with datasets containing non-spherical or arbitrarily shaped clusters (e.g., Moon or Circle).  
  - Requires external methods (Elbow, Silhouette) to determine the number of clusters (*k*).  

- **DBSCAN** (density-based):  
  - Detects clusters of arbitrary shapes and sizes.  
  - Defines clusters based on density connectivity rather than geometric centers.  
  - Uses its own systematic diagnostic method (k-distance graph) to tune parameters (**ε** and **MinPts**).  
  - Generally more robust and adaptable across diverse data structures.  

## Conclusion  
- **K-Medoids**: Simple and effective for well-separated, spherical clusters but limited for complex data.  
- **DBSCAN**: More flexible and powerful for detecting clusters of varying shapes and densities, making it the preferred choice in many real-world scenarios.  
