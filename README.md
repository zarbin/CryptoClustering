# Crypto Clustering - Homework 19
UTA DataViz Bootcamp <br>
03/20/2023

# Summary
The CryptoClustering challenge used an unsupervised learning model to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. Data was preprocessed using the StadardScaler function, and then the best value for *(k)* was determined using the original scaled data and an elbow chart to find best number of clusters to use. Clusters were then plotted using the results.

Afterwards, Principal Cluster Analysis (PCA) Clusters was leveraged to see if we could optimize the clsutering.  *(k)* was plotted using the PCA data and an elbow chart to find best number of clusters to use, and then clusters were plotted using this the results.

After all results were generated we compare the charts side-by-side to determine best approach.

# Work and Findings

Scaled crypto data dataframe
![image](https://user-images.githubusercontent.com/36682023/227012343-8c93ca5d-94af-4192-898a-a4820530e6dd.png)

Used an elbow chart to Find the best value for k using the original data.  It looks like 4 is best.
![image](https://user-images.githubusercontent.com/36682023/227012182-55634347-e8d3-469a-9293-b62ef7f91533.png)

Then we run k-means clusting and produce the below plot.  There are some obvious groupings but data is intermingled a bit.  Let's try to optimize the clusters using PCA (Principal Component Analysis).
![image](https://user-images.githubusercontent.com/36682023/227012133-81bf5635-acfc-4237-8674-8ea2612a8793.png)

PCA Dataframe with 3 principal components. 

![image](https://user-images.githubusercontent.com/36682023/227013037-27c70c42-168d-4a73-b026-7cc4a7bfea05.png)

Used an elbow chart to Find the best value for k using the PCA Dataframe.  It looks like 4 is best again.
![image](https://user-images.githubusercontent.com/36682023/227012089-03c30bdb-b0be-4a50-b948-05836219c931.png)

The PCA optimized clustering creates better clustering when k-means is used. 
![image](https://user-images.githubusercontent.com/36682023/227012041-621e42f0-0008-4fbb-b54e-af5116dd607d.png)

**Question:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

**Answer:** Fewer features allow for clearer clustering to occur and removes the case of cluster 2 (yellow) being embedded within exsiting cluster 3 (green). 
  K-Means works better on the PCA data with fewer features and the results are clear in the visualizaitons as there is tighter grouping and clearer delination between the clusters. 

