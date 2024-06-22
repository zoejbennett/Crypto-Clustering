# Crypto-Clustering
Using unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

This project utilizes K-means clustering techniques to analyze market changes in cryptocurrency models. The code analyzes the effectiveness between analyzing the original dataset using K-means clusters compared to using Principal Component Analysis (PCA). 

To compute each model, the code must have three distinct steps:

1. Instantiate the model: model = Kmeans(n_clusters = i)
2. Fit the model: model.fit(dataframe)
3. Use the model: model.predict(dataframe)

First, to find the value for n_clusters, the code creates an elbow curve model, which demonstrates where the most distinct clusters appear. Here are the results for the elbow curves of both the original and PCA data.

<img width="1083" alt="Screenshot 2024-06-22 at 3 35 40 PM" src="https://github.com/zoejbennett/Crypto-Clustering/assets/157840347/a9ef570b-2394-4373-ba8c-2b479b78e233">

Both show 4 to be the best choice for n_clusters value.

After following the steps above, the graphs below show the results. The original normalized results on the left, and the PCA results on the right.
<img width="1095" alt="Screenshot 2024-06-22 at 3 26 59 PM" src="https://github.com/zoejbennett/Crypto-Clustering/assets/157840347/95261146-914c-4ef6-a321-16e40a5e2bee">

From a visual comparison, the graphs demonstrate a tighter clustered structure in the PCA model. Fewer features tighten the clusters together, but they are still distinguishable. The model performs well while maintaining nearly 90% of the original dataset, and cutting down on processing time and storage.
