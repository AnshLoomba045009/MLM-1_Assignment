# MLM-1_Assignment
1. Project Objectives | Problem Statements
1.1. PO1 | PS1: Performance Analysis:

Clustering players based on their scoring patterns, efficiency, and contribution metrics can help in evaluating player performance from different angles. For example, clusters may reveal groups of players who excel in scoring from particular play types or those who contribute significantly through assists. 1.2. PO2 | PS2: Team Strategy Development:
Understanding player performance clusters can aid coaches and team management in formulating targeted strategies. For instance, identifying clusters of players who excel in offensive plays or those who contribute more through defensive actions can influence game strategies and player rotations. Player Development: Clusters can highlight specific areas of strength and improvement for players. By comparing a player’s cluster with those of top performers, coaches can tailor training programs to address specific weaknesses or further develop strengths. 1.3. PO3 | PS3: Talent Scouting:
For scouts and team managers, clustering provides a quantitative method to compare players and identify potential recruits who fit specific roles within the team. By examining clusters of players not currently on their team, scouts can find undervalued talent or players who meet specific strategic needs. 1.3. PO4 | PS4: Player Performance Segmentation: -Group players based on their performance metrics such as scoring efficiency, defensive actions, and overall contribution to the game. This can help identify players with similar playing styles or effectiveness.
2. Description of Data
2.1. Data Source, Size, Shape

2.1.1. Data Source: Kaggle Dataset
2.1.2. Data Size:
In bytes: 17,069,440
In KB: 16,669.375
2.1.3. Data Shape | Dimension: 26 variables | 82,064 records
2.2. Description of Variables

Index Variable(s): gameid (I1), playerid (I2)
Categorical Variables or Features (CV):
Nominal Type: team (CNV1), home (CNV2), away (CNV3), player (CNV4)
Ordinal Type: type (COV1), season (COV2)
Non-Categorical Variables or Features: MIN (NCV1), %FGA 2PT (NCV2), %FGA 3PT (NCV3), etc.
2.3. Descriptive Statistics

Categorical Variables or Features:
Count | Frequency and Proportion (Relative Frequency) Statistics: Not explicitly calculated.
Non-Categorical Variables or Features:
Measures of Central Tendency and Dispersion: Mean MIN = 23.51, SD MIN = 11.56.
Correlation Statistics: Not provided.
3. Analysis of Data
3.1. Data Pre-Processing

No missing values were detected in the dataset, negating the need for missing data treatment.
Numerical encoding for categorical variables and outlier treatment were not explicitly mentioned.
3.2. Data Analysis

K-Means Clustering (Base Model):
Metrics Used: Euclidean Distance.
Silhouette Score for KMeans with 3 clusters: 0.45324339004077646 -Davies-Bouldin Score for KMeans with 3 clusters: 0.8703766438295721 -Silhouette Score for KMeans with 4 clusters: 0.4662360102564014 -Davies-Bouldin Score for KMeans with 4 clusters: 0.8857993316781488
DBSCAN Clustering (Comparison Model):
Metrics Used: Euclidean Distance.
Silhouette Score: 0.04470008313094927.
Davies-Bouldin Score: 0.7997723640663135.
Cluster Analysis:

K-Means:
Chi-Square Test: No significant association with categorical features (p-value = 1.0).
ANOVA Test: Significant differences among clusters for numerical features (p-value = 0.0).
DBSCAN:
Chi-Square Test: Some significant associations with 'team' feature (p-value = 0.007990638478824199).
ANOVA Test: Significant differences for numerical features (p-value = 0.0).
4. Results | Observations
Appropriate Number of Segments | Clusters:
K-Means: 3 Clusters identified.
DBSCAN: The nature of the algorithm makes it difficult to ascertain a definitive number of clusters.
Cluster Size: Not explicitly stated for either model.
Clustering Model Performance: K-Means outperformed DBSCAN based on the silhouette score, indicating more distinct and better-separated clusters.
Cluster Analysis:
K-Means: No significant associations were found between categorical features and clusters, suggesting that the clusters are not characterized by the categorical features analyzed.
DBSCAN: Some significant associations found, particularly with the 'team' feature, which may influence the cluster formation.
5. Managerial Insights
Appropriate Model: K-Means is deemed more suitable for this dataset given its higher silhouette score, suggesting better-defined clusters compared to DBSCAN.
Appropriate Number of Segments | Clusters: 3 clusters as identified by K-Means appears to be an optimal solution for segmenting the dataset.
Identification of a ‘Niche’ Segment | Cluster: No explicit niche segment was identified, which may require a deeper dive into the clusters' characteristics.
Performance Analysis: Clustering players based on scoring patterns, efficiency, and contribution metrics can provide insights into player performance from different perspectives, such as scoring types and assist contributions.
Team Strategy Development: Understanding player performance clusters can help coaches and team management formulate targeted strategies, such as identifying players for offensive or defensive roles.
Player Development: Clusters can highlight areas of strength and improvement for players, allowing coaches to tailor training programs accordingly.
Talent Scouting: Clustering provides a quantitative method to compare players and identify potential recruits who fit specific roles within the team.
Player Performance Segmentation: Grouping players based on performance metrics can help identify players with similar playing styles or effectiveness.
