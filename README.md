# Bank Customer Churn Prediction

An end-to-end machine learning project focused on predicting customer churn in a banking environment using explainable AI techniques.

---

## Executive Summary

This project develops an end-to-end machine learning solution to predict customer churn in a banking environment. 

Using a Random Forest model optimized for recall, the system identifies high-risk customers before they leave, enabling proactive retention strategies. The model achieves a ROC-AUC of 0.85 and a churn recall of 0.78, ensuring most potential churners are detected.

Beyond prediction, SHAP explainability techniques were applied to uncover the key behavioral drivers of churn, supporting transparent and compliant decision-making in a regulated financial environment.

The project demonstrates how data science can move beyond accuracy metrics and directly inform business strategy, customer engagement, and profitability.


##  Business Problem

Customer churn directly impacts profitability, acquisition costs, and long-term growth.  
The objective is to predict churn early and identify key drivers behind it, enabling proactive and targeted retention strategies.

---

## Business Objectives

- Predict high-risk customers
- Identify early churn signals
- Understand why customers churn (model explainability)
- Reduce false negatives (missed churners)
- Support data-driven decision-making in a regulated environment

---

## Dataset Overview

- Type: Simulated real-world banking dataset
- Records: ~5,000 customers
- Target variable: `churn` (1 = churned, 0 = retained)

### Key Features
- Credit score
- Tenure
- Number of products
- Account balance
- Activity status
- Complaints (last 12 months)

---

## Data Science Workflow

### Data Cleaning
- Handled missing values
- Corrected data types
- Removed duplicates
- Validated target labels

### Exploratory Data Analysis
Key Findings:
- Dataset is imbalanced (~20% churn)
- Inactive customers churn significantly more
- Single-product customers are high risk
- Less products more likely to churn
- Lower account balance more likely to churn
- Complaints strongly correlate with churn

### Feature Engineering
- Created credit score bands
- Encoded categorical variables
- Scaled numerical features

### Modeling
- Logistic Regression (baseline)
- Random Forest (final model)

Why Random Forest?
- Handles non-linear relationships
- Robust to noise
- Performs well with mixed feature types

###  Model Evaluation
Metrics used due to class imbalance:
- Recall
- Precision
- ROC-AUC

**Results:**
- Recall (Churn): 0.78
- ROC-AUC: 0.85

Focus: Minimize false negatives (missed churners).

---

## Model Explainability (SHAP)

SHAP was used to explain:
- Global feature importance
- Individual customer predictions

### Top Churn Drivers
- Low tenure
- Low number of products
- Inactivity
- Recent complaints
- Low account balance

Key Insight:  
Churn is driven more by engagement and service experience than demographics.

---

## Business Impact

- Enables proactive retention strategies
- Reduces customer acquisition costs
- Improves customer lifetime value
- Supports explainable AI compliance in banking

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SHAP

---

##  Project Structure

Bank-Churn-Prediction/
│
├── data/
├── notebooks/
├── README.md
└── requirements.txt

---

## Author

Nhlanhla Lekgale  
Data Science | Machine Learning | Python | Business-Focused AI
