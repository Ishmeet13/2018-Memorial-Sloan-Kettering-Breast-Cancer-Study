# Breast Cancer Genomic Data Analysis

## Overview

This repository contains a comprehensive data science analysis of breast cancer genomic data from the 2018 Memorial Sloan Kettering Cancer Center study. We employ machine learning and statistical techniques to identify genes and mutation patterns associated with clinical outcomes and molecular subtypes.

## Dataset

The analysis uses publicly available data from cBioPortal, including:
- Clinical outcomes and gene mutation information for 1,918 breast cancer patients
- 17,141 genes analyzed
- Patient demographics, tumor pathology, treatment courses, and survival outcomes
- Mutation types including missense, truncating, splice site, and copy number alterations

## Key Features

- **Exploratory Data Analysis**: Comprehensive visualization and summarization of clinical and genomic features
- **Machine Learning Models**: Implementation of Random Forest, Support Vector Machine (SVM), and Naive Bayes algorithms to predict patient survival outcomes
- **Comparative Model Analysis**: Evaluation using ROC curves and AUC metrics (Random Forest: 85% accuracy, AUC 0.87; SVM: 83% accuracy, AUC 0.86)
- **Feature Importance Analysis**: Identification of key genetic markers (TP53, PIK3CA, BRCA1/2 mutations) as significant predictors
- **Relational Data Analysis**: Investigation of gene-gene interactions and subtype-specific mutations
- **Network Analysis**: Identification of previously unreported gene clusters associated with clinical outcomes

## Repository Structure

```
├── data/               # Dataset storage and handling
├── notebooks/          # Jupyter notebooks for analysis
│   ├── 1_EDA.ipynb     # Exploratory Data Analysis
│   ├── 2_ML_Models.ipynb  # Machine Learning Models
│   └── 3_Relational_Analysis.ipynb  # Relational Analysis
├── src/                # Source code
│   ├── preprocessing/  # Data preprocessing utilities
│   ├── models/         # Model definitions
│   └── visualization/  # Visualization scripts
├── results/            # Analysis results and figures
├── requirements.txt    # Project dependencies
└── README.md           # This file
```

## Installation and Usage

### Prerequisites
- Python 3.6+
- Jupyter Notebook
- Required Python packages (see requirements.txt)

```bash
# Clone the repository
git clone https://github.com/[username]/breast-cancer-genomic-analysis.git
cd breast-cancer-genomic-analysis

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook
```

## Machine Learning Models

We implemented three machine learning algorithms to predict patient survival outcomes:

1. **Random Forest**
   - Achieved 85% accuracy
   - AUC: 0.87
   - Identified top predictive genes including TP53, PIK3CA, CDH1

2. **Support Vector Machine (SVM)**
   - Achieved 83% accuracy
   - AUC: 0.86
   - Robust performance across different classification thresholds

3. **Naive Bayes**
   - Achieved 78% accuracy
   - Provided complementary insights into probabilistic relationships

## Key Findings

- Strong correlation between TP53 mutations and overall survival
- Significant co-occurrences between CDH1 and PIK3CA mutations
- Mutual exclusivity between TP53 and PIK3CA/CDH1 mutations
- Distinct mutation patterns in luminal and basal molecular subtypes
- Novel gene clusters associated with clinical outcomes identified through network analysis

## Contributors

- Sachi Khatri (khatri32@uwindsor.ca)
- Ishmeet Singh Arora (arora9e@uwindsor.ca)
- Dhruvi Dobariya (dobariy7@uwindsor.ca)
- Dev Preet Singh (ranjeetd@uwindsor.ca)
- Divy Patel (patel3ma@uwindsor.ca)

## Citation

If you use this code or analysis in your research, please cite our work:

```
@article{khatri2023data,
  title={Data Science Analysis of 2018 Memorial Sloan Kettering Breast Cancer Study},
  author={Khatri, Sachi and Arora, Ishmeet Singh and Dobariya, Dhruvi and Singh, Dev Preet and Patel, Divy},
  journal={},
  year={2023}
}
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Memorial Sloan Kettering Cancer Center for the dataset
- cBioPortal for providing access to cancer genomics data
