# ABC Tech ITSM Analytics

## Project Overview

This project focuses on analyzing IT Service Management (ITSM) incident data for ABC Tech to identify operational patterns, understand incident priorities, forecast incident volumes, and develop data-driven recommendations.

The project uses Python, data analysis, visualization, and machine learning techniques to examine historical ITSM records and support better incident management decisions.

## Business Problem

IT service teams handle large volumes of incidents with different priority levels, categories, and resolution requirements. Without effective analysis, organizations may face challenges in identifying critical incidents, understanding workload patterns, and improving service management processes.

This project explores historical incident data to identify useful insights and evaluate how data analytics and machine learning can support ITSM operations.

## Project Objectives

1. **High-Priority Incident Prediction:** Analyze and develop a machine learning approach to identify high-priority incidents.
2. **Incident Volume Analysis and Forecasting:** Study historical incident trends across different time periods and evaluate future incident volume using a forecasting baseline.
3. **Automatic Priority and Department Tagging:** Evaluate automated priority classification and assess the feasibility of department tagging.
4. **RFC and ITSM Asset Analysis:** Examine related change request information and configuration item patterns to understand the available opportunities and data limitations.
5. **Data-Driven Recommendations:** Translate analytical findings into recommendations for improving IT service management operations.

## Dataset Information

- **Dataset:** ABC Tech ITSM Incident Dataset
- **Records:** 46,606
- **Columns:** 25
- **Time Period:** February 2012 – March 2014
- **Data Type:** Historical IT service incident records

The dataset includes incident status, impact, urgency, priority, category, configuration item information, timestamps, handling time, reassignment counts, and related interaction/change information.

*Note: The original client dataset is not included in this public repository.*

## Technologies and Tools

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Machine Learning
- Exploratory Data Analysis (EDA)
- Time-Series Analysis

## Project Workflow

1. Business understanding
2. Data loading and inspection
3. Data cleaning and preprocessing
4. Exploratory Data Analysis
5. Feature engineering
6. Machine learning model development
7. Model evaluation
8. Incident volume forecasting
9. Business recommendations

## Key Results

### 1. High-Priority Incident Prediction

A Random Forest classification model was developed to identify high-priority incidents.

- Accuracy: 98.28%
- Precision: 44.52%
- Recall: 46.43%
- F1-score: 45.45%

The results indicate that identifying high-priority incidents remains challenging because of class imbalance. The model requires further improvement before operational use.

### 2. Priority Classification

A priority classification model using Impact and Urgency achieved 99.94% accuracy. However, these features largely determine the existing priority level, so this result primarily demonstrates the underlying priority rules rather than independent predictive capability.

Without Impact and Urgency, the model achieved 81.07% accuracy.

### 3. Incident Volume Forecasting

A three-month moving-average baseline was used to estimate incident volumes for April–June 2014.

- April 2014: 7,326
- May 2014: 7,012
- June 2014: 6,890
- Total forecast: 21,228

Evaluation on the January–March 2014 holdout period:

- MAE: 637.44
- RMSE: 728.17

## Project Limitations

- Severe class imbalance affects high-priority incident prediction.
- The dataset contains very few Priority 1 records.
- Department or resolver-group labels are unavailable for department classification.
- Related change request records are sparse.
- Asset failure or misconfiguration outcome labels are unavailable.
- The historical dataset covers a limited period, which restricts forecasting reliability.

## Repository Structure

```text
ABC-Tech-ITSM-Analytics/
│
├── ABC_Tech_ITSM_Analysis.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
└── data/
    └── README.md
```

## How to Run the Project

1. Clone or download this repository.
2. Install Python and Jupyter Notebook.
3. Install the required libraries using:

```bash
pip install -r requirements.txt
```

4. Obtain the dataset through an authorized source.
5. Update the dataset path in the notebook to point to your local dataset.
6. Open `ABC_Tech_ITSM_Analysis.ipynb` in Jupyter Notebook or JupyterLab.
7. Execute the notebook cells in sequence.

## Conclusion

This project demonstrates how data analytics and machine learning can be applied to historical ITSM incident data to identify operational trends, examine priority classification, evaluate high-priority incident prediction, and estimate incident volumes.

It also highlights the importance of data quality, class balance, feature selection, and business context when developing analytical solutions for real-world IT service management problems.

---

**Project Category:** Data Analytics | Machine Learning | IT Service Management

**Tools:** Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn | Jupyter Notebook