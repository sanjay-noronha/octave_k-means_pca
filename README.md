# octave_k-means_pca
Un supervised learning, K means, PCA

IMPORTANT: A very good idea to go back and look at the entire code for this module especially the concept of principal components i.e. eigenvectors.

1. Clustering
    1. K means algorithm
        1. Octave is a free alternative to MATLAB.
        2. Cluster centroids
        3. Number of cost
        4. Optimization - least cost
        5. Elbow method
        6. Select of initial clusters
2. Dimensionality reduction
    1. useful in data viz
    2. PCA algorithm
    3. eigenvectors
    4. co variance matrix
    5. mean normalization- should *ALWAYS* be performed. Feature scaling is optional  . If you do not perform mean normalization, PCA will rotate the data in a possibly undesired way.
    6. feature scaling
    7. projection vector
    8. How to choose k
    9. Going from n -> and k - > n
    10. Do NOT use PCA to reduce features i.e. reduce over-fitting
    11. PCA can be used to improve performance in a supervised learning algo.
    12. PCA should be run on the TRAINING set only and this model can then use used on CV and test. You should not run PCA on CV or test.
3. Practical
    1. K means - use the K-means algorithm for image compression by reducing the number of colors that occur in an image to only those that are most common in that image.
        1. This is a great example which I could not think of
        2. So you have a 128 x 128 pixel images.
        3. Each pixel is 24 bits i..e 8 x 3 bits for each RGB color
        4. So basically 24 bits are used to store each color.
        5. We find the 16 most popular clusters i.e. generate 16 cluster centroids
        6. These are are 16 most popular colors
        7. Now a 4 bit storage is good enough to store an index of 1-16.
        8. So basically we have reduced our 24 bit pixel to 4 bits i.e. by a factor of 6
    2. a low-dimensional representation of face images.
        1. Good use of bsxfun() function for broadcasting explicitly
