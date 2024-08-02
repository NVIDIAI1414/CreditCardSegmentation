# Credit Card Segmentation

Used unsupervised k-means clustering to segment credit card customers based on features available. 

Started by gathering and wrangling data, then log transforming relevant variables so they can be easily scaled by a scaler transformation. A correlation matrix shows strong correlations between credit limit and estimated income, transaction amount, number of transactions and average utilization ratio. 

Some variables like education level were not quantitative ("Uneducated", "High School" etc.) so were mapped to integers with increasing academic proficiency being associated with higher values. Marital status was split into 4 categories and using one-shot-encoding was treated as a binary feature. 

After scaling, a k-means object was created for each 1 < k < 11, with an optimal value at k = 4.

Setting the optimal value = 4, the clusters were identified. In conclusion, they were clustered mainly according to income and marital status/relationships. Cluster 0 corresponded to married people. Cluster 1 corresponded to all marital types with a higher average income overall. Cluster 2 correpsonded to the opposite of cluster 0 (single or divorced people). Cluster 3 corresponded to types of no known marital status who must fall into any of the other 3 categories in reality). 
