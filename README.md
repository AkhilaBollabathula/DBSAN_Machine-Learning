
**Report on Customer Segmentation Analysis Using DBSCAN Clustering**

**Introduction:**
The aim of this report is to perform customer segmentation analysis using the DBSCAN (Density-Based Spatial Clustering of Applications with Noise) algorithm. 
Customer segmentation is a crucial task for businesses as it helps in understanding customer behavior, targeting marketing campaigns, and optimizing business strategies.

** Data Loading and Inspection:**
- The analysis begins with loading the dataset named "Mall_Customers.csv" using the Pandas library.
  
_LIBRARIES USED :
 numpy for numerical computations,
 pandas for data manipulation, 
 analysis seaborn and 
 `matplotlib.pyplot` for data visualization.

- Initial exploration of the dataset includes displaying the first few rows, summary statistics, information about columns, and checking for missing values.

** Data Preprocessing:**
- Data preprocessing steps involve converting the 'Gender' column into numeric format and dropping it from the dataframe since it may not contribute significantly to clustering.
- The 'CustomerID' column is also dropped as it does not provide meaningful information for clustering.

** Exploratory Data Analysis (EDA):**
- A correlation matrix is computed to understand the relationships between numerical features in the dataset.
- A heatmap visualization of the correlation matrix is generated to visually represent the correlations between variables.

** DBSCAN Clustering:**
- DBSCAN clustering is performed on the preprocessed dataset using the `DBSCAN` class from the `sklearn.cluster` module.
- Hyperparameters like 'eps' (maximum distance between two samples for one to be considered as in the neighborhood of the other) and
  'min_samples' (the number of samples in a neighborhood for a point to be considered as a core point) are set empirically.
- The clustering results are assigned to the original dataframe, and a new column 'Cluster' is added to indicate the cluster label for each data point.

** Analysis of Clustering Results:**
- The size of each cluster is computed and visualized to understand the distribution of data points across different clusters.
- Outliers, if any, are identified as data points labeled as '-1' (noise) by DBSCAN.
- A scatter plot is created to visualize the clusters based on 'Annual Income' and 'Spending Score', with outliers represented separately.

**Conclusion:**
In conclusion, the DBSCAN algorithm effectively segments customers based on their 'Annual Income' and 'Spending Score'.The identified clusters can provide valuable
insights for targeted marketing strategies, personalized customer experiences, and product recommendations.However, further analysis, such as interpretation of cluster 
characteristics and comparison with domain knowledge, is recommended for a more comprehensive understanding of customer behavior.





