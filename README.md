# Cryptocurrencies
## Overview 
The client,Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers.  They have requested a report which details cryptocurrencies on the trading market and classfication system of those cryptocurrenices.  To accomplish this request, unsupervised learning will be implemented.  Clustering algortthim will be used to group the cryptocurrencies.  The data has be preprocessed for PCA.  Next the data dimensions were reduced using PCA.  The cryptocurrencies were then clustered by the use of K-means.  Finally, cryptocurrencies results were visualizied.     
## Results
### Preprocessing the Data for PCA
The data of cryptocurrecies was filtered for cryptocurrencies being traded, dropping row with at least one null value and coins that have been mined.  After the data was filtered, a seperate dataframe was established with only the names of cryptocurrency(used later in the clustering algorithm).  get_dummies() method was used two create two variables (columns of Algorithm and ProofType) which were stored in a new DataFrame (X).  X's feature were standardizwd by use of StandardScaler fit_transform().  This created a new DataFrame X_scaled
###  Reducing Data Dimensions Using PCA 
PCA was applied to reduce the dimensions of X_scaled dataframe into to three principal componets.  New DataFrame was created using results of PCA with same index of orginal dataframe.
### Clustering Cryptocurrencies Using K-means
An elbow curve was created from PCA DataFrame.  Results of the elbow curve show that k=4 which meant that n_cluster of K-means algorithm should be set to this value.  Below is the elbow curve graph.
![alt txt]()
 
PCA DataFrame used to run the K-means algorithm to make predictions of K clusters of the data.  A new DataFrame was  made by using pd.concat(concatenating) on orginal DataFrame and PCA DataFrame. Coin names created earlier were added to the new DataFrame.  The predictions created early were set as column called Class.   
![alt txt]()

### Visualizing Cryptocurrencies Results 
* 3D-Scatter with the PCA data and the clusters
![alt txt]()

* Sortable and Selectable Table of Tradable Cryptocurrencies
![alt txt]()

* Detemined that were 532 tradable cryptocurrencies.

* New DataFrame consisting of the scaled data with the clustered_df DataFrame including coin name and class
![alt txt]()

* Scatterplot with x="TotalCoinsMined", y="TotalCoinSupply", and by="Class", and have it show the CoinName when you hover over the the data point
![alt txt]()

 