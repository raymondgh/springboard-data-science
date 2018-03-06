# Clustering: Customer Segmenetation

[Python Notebook](Mini_Project_Clustering.ipynb)

### Assignment

This exercise demonstrates wine customer segmentation using unsupervised learning clustering techniques to create data-driven personas regarding buying behavior.

### Data

324 transaction records including customer names and details loaded from an Excel file. 32 company offer records including discount amount and other details loaded from an Excel file.

### Approach

First, the data is "wrangled" into tidy data samples of customers with offer-elections as boolean values. These offer-elections are the explanatory factors subsequently used for K-Means clustering. Tuning the number of clusters is practiced through three methods: The Elbow Method, The Silhouette Method, and visual scatterplots. It is shown that selecting a number of clusters is not necessarily a straightforward process, but rather requires meaningful understanding of the dataset and and judgement of the purpose of the analysis. Cohorts of customers are created based on four clusters and analyzed after merging the cluster data back into the original transaction data. In the end, a handful of other clustering methods are tried and scored by Silhouette score.

### Reflection

It seems to me that a lot of the hyperparameter tuning and visualization could be further automated a la gridsearch and pipeline management. I would expect a company with a robust understanding of their data to have engineered systems by which new features significance and clusters can emerge without major re-work. I would also add that's it's pretty fun to start with a list of receipts and end up with very strong mental images of different types of customers! This would be great for the marketing team.
