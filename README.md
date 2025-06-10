Customer Segmentation Report
Executive Summary:
This project applied clustering (K-Means) on telecom customer data to identify actionable segments. Cleaned
data, selected features, and dimensionality reduction were followed by robust cluster profiling and business
recommendations.
1. Data Exploration & Missing Values
- Data types verified.
- No missing values except 'TotalCharges' where blank entries were found for new users (tenure = 0).
- These rows were dropped (if minimal) for better model performance.
- Justification: they lack behavioral signals and can distort cluster structure.
2. Feature Engineering
- 19 features selected: demographics, services, contracts, usage.
- One-hot encoding used (drop_first=True) for categorical variables.
- StandardScaler applied on numerical columns to ensure fair clustering.
- Scaling is essential for distance-based algorithms like K-Means.
3. Dimensionality Reduction
- PCA applied to retain 95% variance.
- Dimensionality reduced from 39 to 21 features.
- Helped improve clustering quality and enabled 2D visualization.
4. Clustering Approach
- Algorithm: K-Means (simple, scalable, interpretable).
- k chosen using Elbow Method & Silhouette Score -> Optimal at k = 3.
- Validated cluster stability using multiple random seeds (0 to 4).
5. Cluster Profiling
Customer Segmentation Report
Cluster 0 - Budget-conscious: low tenure, low charges, DSL users, short contracts.
Cluster 1 - Mid-range Loyalists: balanced usage, mid-level tenure and charges.
Cluster 2 - High-Value Users: long tenure, high charges, fiber, 2-year contracts.
Labels: Budget-conscious, Mid-range Loyalists, High-Value Users.
6. Visualization Summary
- PCA plot showed clear cluster separation.
- Boxplots: Tenure & MonthlyCharges by cluster.
- Countplots: InternetService & Contract types by cluster.
- Insightful visual differences support business actions.
7. Stakeholder Recommendations
| Segment | Recommendation |
|---------------------|--------------------------------------------------|
| Budget-conscious | Short-term offers, entry-level bundles |
| Mid-range Loyalists | Upsell additional services (e.g. tech support) |
| High-Value Users | Loyalty programs, high-value retention offers
Next Steps
1. Integrate clusters into CRM system.
2. Personalize campaigns by segment.
3. Track churn and upsell conversion to evaluate impact.
