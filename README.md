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
### 2. Running the Pipeline
Open the project in JupyterLab:

