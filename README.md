<div align="center">

# 📊 Customer Segments Analysis

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Latest-green?style=for-the-badge&logo=scikit-learn)](https://scikit-learn.org/)

*An unsupervised learning project to identify core customer segments from German demographics data*


</div>

---

## 📌 Overview
This project employs advanced machine learning techniques to analyze demographics data and identify distinct customer segments for a German mail-order sales company. Through comparative analysis of general population data with existing customer profiles, we uncover over-represented customer groups to enable data-driven marketing strategies.

### 🎯 Why Customer Segmentation?
Customer segmentation empowers businesses to:
- 📈 Develop targeted marketing strategies for specific demographic groups
- 🤝 Enhance customer engagement through personalized messaging
- 💰 Optimize marketing budget allocation
- 🔍 Uncover hidden patterns in customer behavior
- 📊 Make data-driven business decisions

## 📚 Data Sources
The analysis leverages four comprehensive datasets:

| Dataset | Description | Size | Features |
|---------|-------------|------|----------|
| `Udacity_AZDIAS_Subset.csv` | General population demographics | 891,211 persons | 85 features |
| `Udacity_CUSTOMERS_Subset.csv` | Customer demographics | 191,652 persons | 85 features |
| `Data_Dictionary.md` | Feature descriptions | - | - |
| `AZDIAS_Feature_Summary.csv` | Feature attributes summary | - | - |

### 📋 Feature Categories
1. **Personal Attributes**
   - Age
   - Gender
   - Marital status
   - Education level

2. **Household Information**
   - Income bracket
   - Family type
   - Number of children
   - Living situation

3. **Regional Characteristics**
   - Building type
   - Neighborhood demographics
   - Urban/rural classification
   - Regional economic indicators

## 🚀 Installation

### System Requirements
- Python 3.7+
- Git
- 8GB RAM minimum
- 50GB free disk space

### Required Libraries
```bash
pandas==1.3.3
numpy==1.21.2
matplotlib==3.4.3
seaborn==0.11.2
scikit-learn==0.24.2
jupyter==1.0.0
```

### Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/YaraDaraghmeh/identify-customer-segments.git
   cd identify-customer-segments
   ```

2. Create and activate virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Download datasets:

## 💻 Usage

### Getting Started
1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook Identify_Customer_Segments.ipynb
   ```

2. Execute notebook sections:
   - Data loading and exploration
   - Preprocessing and cleaning
   - Feature engineering
   - Dimensionality reduction
   - Cluster analysis
   - Results visualization

### Project Structure
```
identify-customer-segments/
├── data/                  # Dataset directory
├── notebooks/            # Jupyter notebooks
├── scripts/              # Utility scripts
├── results/              # Output files
├── requirements.txt      # Dependencies
└── README.md            # This file
```

## 🔬 Methodology

### 1. Data Preprocessing
- **Missing Value Treatment**
  - Convert encoded missing values to NaN
  - Drop columns with >30% missing data
  - Remove rows with >10 missing values
  - Advanced imputation techniques for remaining gaps

- **Feature Engineering**
  - Impute missing values using median/mode
  - One-hot encode categorical variables
  - Standardize numerical features
  - Create derived features from existing attributes

### 2. Dimensionality Reduction
- Apply PCA to reduce 85 features to 30 principal components
- Retain approximately 85% of variance
- Analyze component interpretations for demographic insights
- Validate reduction impact on data integrity

### 3. Clustering Analysis
- Implement K-Means clustering
- Use Elbow Method and Silhouette Analysis for optimal cluster count
- Validate cluster stability
- Compare cluster distributions between populations

## 📊 Results

### Key Findings
- Identified two primary target segments (Clusters 3 and 5)
- Target segments show 2.5x higher representation in customer base
- Discovered significant demographic patterns:
  - Age distribution peaks
  - Income level correlations
  - Regional preferences

### Target Segment Characteristics
1. **Cluster 3: Urban Professionals**
   - High-income households
   - City centers
   - Active lifestyle indicators
   - Strong financial planning focus

2. **Cluster 5: Suburban Families**
   - Middle-aged parents
   - Stable employment
   - Home ownership
   - Family-oriented purchasing patterns

## 📈 Future Improvements
1. Incorporate additional data sources
2. Experiment with alternative clustering algorithms
3. Develop real-time segmentation capabilities
4. Create interactive visualization dashboard

## 🤝 Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 👏 Acknowledgments
- Data provided by Bertelsmann Arvato Analytics
- Project guidance from Udacity Data Scientist Nanodegree Program
- Community feedback and contributions

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Created with ❤️ by [Yara Dababat](https://github.com/YaraDaraghmeh)

⭐️ Star this project if you find it useful!

</div>
