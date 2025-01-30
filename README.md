# Customer Segments Analysis

A data science project that uses unsupervised learning to identify core customer segments from German demographics data.

## Overview

This project analyzes demographics data to identify distinct customer segments for a German mail-order sales company. By comparing general population data with existing customer profiles, we identify over-represented customer groups to enable targeted marketing strategies.

### Why Customer Segmentation?

Customer segmentation allows businesses to:
- Tailor marketing strategies to specific demographic groups
- Improve customer engagement through targeted messaging
- Optimize marketing resource allocation
- Discover hidden patterns in customer behavior

## Data Sources

The analysis uses four primary datasets:

| Dataset | Description | Size | Features |
|---------|-------------|------|----------|
| `Udacity_AZDIAS_Subset.csv` | General population demographics | 891,211 persons | 85 features |
| `Udacity_CUSTOMERS_Subset.csv` | Customer demographics | 191,652 persons | 85 features |
| `Data_Dictionary.md` | Feature descriptions | - | - |
| `AZDIAS_Feature_Summary.csv` | Feature attributes summary | - | - |

Features include person-level attributes (age, gender), household information (income, family type), and regional characteristics (building type, neighborhood).

## Installation

### Prerequisites

- Python 3.7+
- Git

### Required Libraries

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/YaraDaraghmeh/identify-customer-segments.git
   cd identify-customer-segments
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the datasets and place them in the `data/` directory

## Usage

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook Identify_Customer_Segments.ipynb
   ```

2. Execute the notebook cells sequentially to:
   - Preprocess the demographics data
   - Reduce dimensionality using PCA
   - Perform clustering analysis
   - Compare population and customer segments

## Methodology

### 1. Data Preprocessing

- **Missing Value Treatment**
  - Convert encoded missing values to NaN
  - Drop columns with >30% missing data
  - Remove rows with >10 missing values
  
- **Feature Engineering**
  - Impute missing values using median/mode
  - One-hot encode categorical variables
  - Standardize numerical features

### 2. Dimensionality Reduction

- Apply PCA to reduce 85 features to 30 principal components
- Retain approximately 85% of variance
- Analyze component interpretations for demographic insights

### 3. Clustering Analysis

- Implement K-Means clustering
- Use Elbow Method to determine optimal cluster count
- Compare cluster distributions between general population and customers

## Results

Key findings from the analysis:

- Identified two primary target segments (Clusters 3 and 5)
- Target segments show 2.5x higher representation in customer base
- Key characteristics of target segments:
  - High-income urban households
  - Middle-aged families with financial planning focus



## Acknowledgments

- Data provided by Bertelsmann Arvato Analytics
- Project guidance from Udacity Data Scientist Nanodegree Program

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
