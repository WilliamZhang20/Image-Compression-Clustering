﻿# Image-Compression-Clustering

Applied [K-means clustering](https://stanford.edu/~cpiech/cs221/handouts/kmeans.html) to an image to compress it from many colors to only 16 colors.

## Background

A large variety of colors requires more bits to store for all pixels. Since each pixel contains scaling for Red, Green, and Blue (RGB) values, compression reduces it to storing only 16 possible RGB tuples rather than many. 

To do this, the K-means clustering algorithm groups each pixel, a vector in 3D space, with one of 16 centroids - a single point in 3D space representing an RGB color that replaces the associated pixel in the compressed image.

The algorithm will proceed as follows:
1. Randomly initialize K centroids in the data space. In our case, it is 16 centroids for 16 colors in 3D RGB space.
2. For a certain number of iterations:
   a. Assign each data point to the closest centroid.
   b. Compute the mean of the data points assigned to each centroid. This is the new location of that centroid.
3. With a good enough initialization of centroids, the centroids and their groupings should converge to a compact pattern with low distortion & variance.

## Results

### A 3D plot of the centroids after 9 iterations:

![image](https://github.com/user-attachments/assets/9a8a4d81-5ed3-4250-82da-1f5e22f5601e)

### Original & Reconstructed Images:

![image](https://github.com/user-attachments/assets/3aad0897-b820-4687-aeeb-ef65b7cd4fbe)
