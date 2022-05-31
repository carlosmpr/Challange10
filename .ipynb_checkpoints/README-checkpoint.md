# Crypto Advisor
In this Challenge, you’ll combine your financial Python programming skills with the new unsupervised learning skills that you acquired in this module.
You’ll create a Jupyter notebook that clusters cryptocurrencies by their performance in different time periods. You’ll then plot the results so that you can visually show the performance to the board.

## The steps:


- Prepare the Data 
- Find the Best Value for `k` Using the Original Data
- Cluster Cryptocurrencies with K-means Using the Original Data
* Optimize Clusters with Principal Component Analysis
* Find the Best Value for `k` Using the PCA Data
* Cluster the Cryptocurrencies with K-means Using the PCA Data
* Visualize and Compare the Results
---

## 1. Prepare the Data


This section prepares the data before running the K-Means algorithm. It follows these steps:

1. Used the `StandardScaler` module from scikit-learn to normalize the CSV file data. This will require you to utilize the `fit_transform` function.

2. Created a DataFrame that contains the scaled data. Be sure to set the `coin_id` index from the original DataFrame as the index for the new DataFrame.

---

## 2. Find the Best Value for k Using the Original Data

In this section, you will use the elbow method to find the best value for `k`.

1. Coded the elbow method algorithm to find the best value for `k`. Used a range from 1 to 11. 

2. Ploted a line chart with all the inertia values computed with the different values of `k` to visually identify the optimal value for `k`.



---

## 3. Cluster Cryptocurrencies with K-means Using the Original Data

In this section, you will use the K-Means algorithm with the best value for `k` found in the previous section to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.

1. Initialized the K-Means model with four clusters using the best value for `k`. 

2. Fited the K-Means model using the original data.

3. Predicted the clusters to group the cryptocurrencies using the original data. View the resulting array of cluster values.

4. Created a copy of the original data and add a new column with the predicted clusters.

5. Created a scatter plot using hvPlot by setting `x="price_change_percentage_24h"` and `y="price_change_percentage_7d"`. Color the graph points with the labels found using K-Means and add the crypto name in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

---

## 4.  Optimize Clusters with Principal Component Analysis

In this section, perform a principal component analysis (PCA) and reduce the features to three principal components.

1. Created a PCA model instance and set `n_components=3`.

2. Used the PCA model to reduce to three principal components. View the first five rows of the DataFrame. 

3. Retrieved the explained variance to determine how much information can be attributed to each principal component.

5. Created a new DataFrame with the PCA data. Be sure to set the `coin_id` index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.


---
## 5.  Find the Best Value for k Using the PCA Data

In this section, you will use the elbow method to find the best value for `k` using the PCA data.

1. Coded the elbow method algorithm and use the PCA data to find the best value for `k`. Use a range from 1 to 11. 

2. Ploted a line chart with all the inertia values computed with the different values of `k` to visually identify the optimal value for `k`.



---

## 6. Cluster Cryptocurrencies with K-means Using the PCA Data

In this section, you will use the PCA data and the K-Means algorithm with the best value for `k` found in the previous section to cluster the cryptocurrencies according to the principal components.

1. Initialized the K-Means model with four clusters using the best value for `k`. 

2. Fited the K-Means model using the PCA data.

3. Predicted the clusters to group the cryptocurrencies using the PCA data. View the resulting array of cluster values.

4. Added a new column to the DataFrame with the PCA data to store the predicted clusters.

5. Created a scatter plot using hvPlot by setting `x="PC1"` and `y="PC2"`. Color the graph points with the labels found using K-Means and add the crypto name in the `hover_cols` parameter to identify the cryptocurrency represented by each data point.

---

## 7.  Visualize and Compare the Results

In this section, you will visually analyze the cluster analysis results by contrasting the outcome with and without using the optimization techniques.

1. Created a composite plot using hvPlot and the plus (`+`) operator to contrast the Elbow Curve that you created to find the best value for `k` with the original and the PCA data.

2. Created a composite plot using hvPlot and the plus (`+`) operator to contrast the cryptocurrencies clusters using the original and the PCA data.



--- 


##  Contributors
Brought to you by Carlos Polanco.

- Email: carlos.polanco0508@gmail.com
- GithubProfile: https://github.com/carlosmpr
- Linkedin: https://www.linkedin.com/in/carlosmpr/

---

## License

MIT

Copyright (c) 2012-2022

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.