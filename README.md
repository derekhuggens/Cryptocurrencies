# Cryptocurrencies
Unsupervised Machine Learning: Transformations and Clustering, K-Means, Centroids, Elbow Curve and more.<br>

## Purpose<br>

The purpose of this repository is to showcase the preprocessing of cryptocurrency data (Source: https://min-api.cryptocompare.com/data/all/coinlist) for Principal Component Analysis and its use in reducing data dimensionality. Clustering with K-Means is also shown using the Elbow Curve method to find the best K-value. After initiating a KMeans model, fitting the model, and making predictions with the corresponding PCA DataFrame, a concatenated DataFrame was created that held predicted clusters, features, cryptocurrency names, and associated model class labels. <br>

### 3-D Scatter Plot with Clusters<br>

From this concatenated DataFrame, visualizations were made using `px.scatter_3d`.<br>

![3d_clusters](https://github.com/derekhuggens/Cryptocurrencies/blob/b39054287ed9f54f3cc34c10f436e31eea853839/README_IMAGES/3d_scatter_clusters.png)<br><br>

### Sortable Table<br>

A table was made with `hvplot.table` showing tradable cryptocurrencies.<br>

![hvplot.table](https://github.com/derekhuggens/Cryptocurrencies/blob/b39054287ed9f54f3cc34c10f436e31eea853839/README_IMAGES/hvplot.table.png)<br><br>

### 2-D Scatter Plot

Two existing columns, `TotalCoinSupply` and `TotalCoinsMined`, were transformed between 0 and 1 using `MinMaxScaler()` and `.fit_transform()`. These two columns were added to a new DataFrame along with two additional columns, `CoinName` and `Class`, to visualize using `.hvplot.scatter`.

![hvplot.scatter](https://github.com/derekhuggens/Cryptocurrencies/blob/b39054287ed9f54f3cc34c10f436e31eea853839/README_IMAGES/hvplot.scatter.png)
