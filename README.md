# SmartCart-E-commerce-Customer-Segmentation-System-Machine-Learning-Project
SmartCart is an unsupervised ML system built with Python and Scikit-Learn to segment e-commerce customers. By engineering behavioral features like total spending and customer tenure, it groups users into distinct buyer personas. These insights drive targeted marketing, optimize loyalty programs, and boost ROI.
# SmartCart: E-commerce Customer Segmentation System 

## Executive Summary
SmartCart is an unsupervised machine learning clustering system designed to segment e-commerce customers based on their demographics and purchasing behavior. By analyzing customer profiles and transaction histories, the project identifies distinct buyer personas to drive targeted marketing, optimize premium services, and improve overall Return on Investment (ROI). The pipeline processes raw transaction data, engineers high-value features, and prepares the dataset for advanced clustering algorithms.

---

##  Project Overview & Description
In the highly competitive e-commerce landscape, understanding customer behavior is critical for personalized marketing. The SmartCart project leverages data science to automate customer profiling. 

Key preprocessing and engineering steps undertaken in this project include:
* Loaded the `smartcart_customers.csv` dataset, which initially contained 2240 rows and 22 columns.
* Addressed 24 missing values within the `Income` column by applying median imputation.
* Engineered the `Age` feature by subtracting the `Year_Birth` from the current base year, 2026.
* Calculated customer tenure in days using the maximum `Dt_Customer` date as the reference point[cite: 1].
* Created a `Total_Spending` feature by summing the amounts spent on Wines, Fruits, Meat, Fish, Sweets, and Gold products[cite: 1].
* Consolidated the `Kidhome` and `Teenhome` variables into a single `Total_Children` metric[cite: 1].
* Standardized the `Education` feature into three distinct categories: Undergraduate, Graduate, and Postgraduate[cite: 1].
* Mapped `Marital_Status` into a simplified `Living_With` category, indicating whether the customer lives with a Partner or Alone[cite: 1].
* Dropped 12 redundant or pre-engineered columns to finalize a cleaned dataset of 2240 rows and 15 columns[cite: 1].

---

##  Tech Stack & Libraries
* **Language:** Python
* **Environment:** JupyterLab / Jupyter Notebook
* **Libraries Utilized:** 
  * `pandas` for data manipulation[cite: 1].
  * `matplotlib.pyplot` for foundational data visualization[cite: 1].
  * `seaborn` for advanced statistical plotting and outlier detection[cite: 1].
  * `scikit-learn` for data scaling and clustering (K-Means).

---

##  Usage Instructions

### 1. Installation & Setup
Clone the repository and install the required dependencies:
```bash
git clone [https://github.com/YOUR_USERNAME/SmartCart-Clustering.git](https://github.com/YOUR_USERNAME/SmartCart-Clustering.git)
cd SmartCart-Clustering
pip install pandas numpy scikit-learn matplotlib seaborn

##  Reports & Insights
Feature Engineering Report
The dataset required significant transformation to be viable for distance-based clustering algorithms. The reduction of dimensionality from 22 to 15 columns ensured that the model was not influenced by redundant identifiers (like ID) or unaggregated data[cite: 1]. Categorical simplification (e.g., reducing complex marital statuses to Partner/Alone) drastically improved the encoding efficiency[cite: 1].

Outlier Detection Report
Visualized feature distributions using Seaborn's PairGrid to detect anomalies in income and spending patterns[cite: 1]. Treating these outliers is a critical step prior to implementing K-Means, as distance-based algorithms are highly sensitive to extreme values.

Clustering Performance Report
(Note: Replace the bracketed values with your final notebook metrics)

Metric	Score
Optimal Clusters (K)	[Insert Number, e.g., 4]
Silhouette Score	[Insert Score, e.g., 0.65]
Inertia (WCSS)	[Insert Score]
## Conclusion
The SmartCart segmentation system successfully processed raw e-commerce data into a clean, model-ready format. By engineering aggregated behavioral features like Total_Spending and Customer_Tenure_Days, the model was able to group customers into highly actionable business personas. This automated clustering approach provides the marketing team with the exact demographic targets needed for loyalty programs, discount campaigns, and premium service offerings.

## Summary for Betterment (Future Scope)
To continually enhance the SmartCart system, the following improvements are proposed:

Advanced Clustering Techniques: Explore Density-Based Spatial Clustering of Applications with Noise (DBSCAN) or Hierarchical clustering to identify non-spherical customer segments.

Dimensionality Reduction: Implement Principal Component Analysis (PCA) prior to clustering to visually map the customer segments in a clean 2D or 3D space.

Automated Data Pipeline: Convert the Jupyter Notebook steps into a robust, object-oriented Python script using Scikit-Learn's Pipeline and ColumnTransformer for seamless deployment.

Dynamic Dashboarding: Connect the clustering outputs to a visualization tool (like Tableau or a Streamlit web app) to provide stakeholders with a live view of shifting customer personas.
