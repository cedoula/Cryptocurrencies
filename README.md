# Cryptocurrencies

## Analysis Overview
The purpose of this project is to use unsupervised machine learning to analyze a database of cryptocurrencies and create a report including the traded cryptocurrencies classified by group according to their features.\
This classification report could be used by an investment bank to propose a new cryptocurrency investment portfolio to its clients.\
We use the following methods for the analysis:
- preprocessing the database,
- reducing the data dimension using Principal Component Analysis,
- clustering cryptocurrencies using K-Means,
- visualizing classification results with 2D and 3D scatter plots.
<br><br>

## Resources
- Data Source: [crypto_data.csv](https://github.com/cedoula/Cryptocurrencies/blob/main/Resources/crypto_data.csv), [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)
- Software: Python 3.7.7, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3
<br><br>

## Results
Following the preprocessing and cleaning phase we have a total of 532 tradable cryptocurrencies.
<br><br>

### Clustering Cryptocurrencies using K-Means - Elbow Curve
We don't know what would be the output of the analysis so we are using unsupervised machine learning to identify clusters of the cryptocurrencies.\
We produced the elbow curve below using the K-Means method iterating on k values from 1 to 10. 
<p align="center">
    <img src="https://user-images.githubusercontent.com/68669675/101305766-01251280-3809-11eb-92f0-0ecb880db7fe.png"> 
</p>
The best k value appears to be 4 so we would conclude on an output of 4 clusters to categorize the crytocurrencies.
<br><br>

### Visualizing Cryptocurrencies Results
#### 3D-Scatter plot with clusters
<p align="center">
    <img src="https://user-images.githubusercontent.com/68669675/101305762-008c7c00-3809-11eb-9c47-95b4d582b784.png"> 
</p>
This 3-D scatter plot was obtained using the PCA algorithm to reduce the crytocurrencies dimensions to three principal components.
<br><br>

#### 2D-Scatter plot with clusters
<p align="center">
    <img src="https://user-images.githubusercontent.com/68669675/101305760-fff3e580-3808-11eb-9614-12a0102ed1f6.png"> 
</p>
This 2-D scatter plot was obtained using the PCA algorithm to reduce the crytocurrencies dimensions to two principal components.
<br><br>
Both these scatter plots show the distribution and the four clusters of cryptocurrencies.<br>
We can identify the outliers like the unique cryptocurrency in the class #2.
<br><br>

#### Tradable Cryptocurrencies Table
<p align="center">
    <img src="https://user-images.githubusercontent.com/68669675/101307931-41d35a80-380e-11eb-942f-7a8f23887d05.png"> 
</p>
Most of the cryptocurrencies are part of class #0 and #1.<br>
The snapshot above shows that BitTorrent is the only cryptocurrency in class #2.
<br><br>

#### 2D-Scatter plot with TotalCoinMined vs TotalCoinSupply
<p align="center">
    <img src="https://user-images.githubusercontent.com/68669675/101305764-008c7c00-3809-11eb-8bd7-85bc2c8e953e.png"> 
</p>
Plotting the scatter plot from two cryptocurrency features directly does not efficiently segregate the different classes. Then using the PCA algorithm is the right method for better visualizations.
<br><br>

## Summary
We have identified the classification of 532 cryptocurrencies based on similarities of their features.\
Particularities of each group need to be analyzed to determined their performance and potential interest for the investment bank's clients.