### K-Means Clustering for Customer Segmentation

This project utilizes K-Means clustering to segment customers based on their annual income and spending scores, helping to identify distinct customer groups.

#### Project Overview
- **Dataset**: `Mall_Customers.csv`, containing data on customer demographics and purchasing behavior.
- **Goal**: To apply K-Means clustering to group customers into meaningful segments based on their spending habits and annual income.

#### Code Breakdown
1. **Import Libraries**: 
   - Essential Python libraries are imported, including `numpy`, `pandas`, `matplotlib`, and `seaborn` for data handling and visualization.
   - `KMeans` from `sklearn.cluster` is used for clustering.

2. **Data Preparation**:
   - The dataset is read using `pd.read_csv()`, and the shape and initial rows are inspected.
   - Feature extraction: The data is prepared by selecting the 'Annual Income' and 'Spending Score' columns for clustering (`X`).

3. **Finding Optimal Number of Clusters**:
   - The **Elbow Method** is used to find the ideal number of clusters. This method involves plotting the **Within-Cluster Sum of Squares (WCSS)** for different values of `k` (number of clusters) and identifying the "elbow point" where the WCSS starts to decrease more slowly.
   - The `KMeans` model is fitted iteratively from 1 to 10 clusters, and WCSS values are stored and visualized with `matplotlib` and `seaborn`.

4. **Model Training**:
   - The K-Means model is trained with `n_clusters=5` (based on the elbow point) using the `k-means++` initialization to optimize cluster placement.

5. **Visualization**:
   - Customer segments are plotted using a scatter plot, with each cluster represented by a unique color.
   - Cluster centroids are marked for reference.

#### Visuals
- **Elbow Point Graph**: Shows the optimal number of clusters using the WCSS plot.
- **Customer Segmentation Plot**: Visualizes the customer clusters in a scatter plot with distinct colors and labeled centroids.

This project provides insight into customer groupings, which can be leveraged for targeted marketing strategies and better business decision-making.
