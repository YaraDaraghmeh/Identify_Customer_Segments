# Identify Customer Segments

## Table of Contents
- [Project Overview](#project-overview)
- [Data](#data)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [Project Structure](#project-structure)
- [Acknowledgments](#acknowledgments)
- [License](#license)

---

## Project Overview
This project applies **unsupervised learning techniques** to identify customer segments within the demographics of a mail-order sales company in Germany. The goal is to analyze the general population and existing customer data to find **core customer groups** that are over-represented among customers. These insights can direct targeted marketing campaigns to maximize returns. 

**Why Customer Segmentation?**  
Segmentation helps businesses tailor strategies to specific groups, improving engagement and efficiency. Clustering is ideal for discovering hidden patterns in unlabeled data, making it perfect for this use case.

---

## Data
The project uses four datasets:
1. **`Udacity_AZDIAS_Subset.csv`**: Demographics data for the general population (891,211 persons, 85 features).  
2. **`Udacity_CUSTOMERS_Subset.csv`**: Demographics data for customers (191,652 persons, 85 features).  
3. **`Data_Dictionary.md`**: Detailed descriptions of all features (e.g., household, building, neighborhood attributes).  
4. **`AZDIAS_Feature_Summary.csv`**: Summary of feature attributes, including encoded missing values (e.g., `-1`, `0`, `9`).  

### Key Data Characteristics
- **Features**: Include person-level (age, gender), household (income, family type), and regional (building type, neighborhood) attributes.  
- **Missing Values**: Encoded with placeholders (e.g., `-1`, `0`, `XX`), converted to `NaN` during preprocessing.  

---

## Installation

### Dependencies
- **Python 3.7+**
- Libraries:  
  ```bash
  pandas numpy matplotlib seaborn scikit-learn jupyter

  Setup
Clone the repository:

bash
Copy
git clone https://github.com/your-username/identify-customer-segments.git
cd identify-customer-segments
Install dependencies:

bash
Copy
pip install -r requirements.txt  # Optional: Create a virtual environment first
Download datasets from Udacity and place them in the data/ directory.

sage
Launch Jupyter Notebook:

bash
Copy
jupyter notebook Identify_Customer_Segments.ipynb
Execute Cells Sequentially:

Data Preprocessing: Clean missing values, encode features, and standardize data.

Dimensionality Reduction: Apply PCA to reduce feature space.

Clustering: Use K-Means to segment the population.

Analysis: Compare customer vs. population clusters to identify target groups.

Methodology
1. Data Preprocessing
Handling Missing Values:

Convert encoded values (e.g., -1, 0) to NaN using AZDIAS_Feature_Summary.csv.

Drop columns with >30% missing data and rows with >10 missing values.

Feature Engineering:

Imputation: Fill missing values using median (numerical) or mode (categorical).

Encoding: One-hot encode categorical variables (e.g., OST_WEST_KZ).

Standardization: Scale features using StandardScaler.

2. Dimensionality Reduction (PCA)
Reduce 85 features to 30 principal components, retaining ~85% variance.

Visualize components to interpret demographic trends.

3. Clustering (K-Means)
Use the Elbow Method to determine optimal clusters (e.g., k=5).

Fit model on the general population and predict clusters for customers.

Key Metric: Compare cluster distributions to identify over-represented customer segments.

Results
Cluster 3 and Cluster 5 were 2.5x more prevalent in customer data vs. the general population.

Key Characteristics of target clusters:

High-income households in urban areas.

Middle-aged families with a focus on financial planning.

Visualizations:

PCA component analysis (e.g., Component 1 correlates with wealth).

Cluster distribution bar charts (population vs. customers).

PCA Visualization
Example: PCA Components Explained Variance
cknowledgments
Data Provided By: Bertelsmann Arvato Analytics.

Project Guidance: Udacity Data Scientist Nanodegree Program.

Libraries: pandas, scikit-learn, matplotlib.
