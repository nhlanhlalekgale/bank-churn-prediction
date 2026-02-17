# Bank Customer Churn Prediction

## Executive Summary
This project develops an end-to-end machine learning solution to predict customer churn in a banking environment using a structured dataset of 5,000 customers.  

Multiple models were evaluated, including Logistic Regression, Random Forest, Gradient Boosting, and XGBoost. Logistic Regression achieved the highest ROC-AUC score (0.775), outperforming more complex ensemble methods.  

Classification threshold optimization was performed to align predictions with business retention objectives, demonstrating how model deployment decisions influence operational strategy.  

This project emphasizes disciplined model comparison, interpretability, and business-aligned decision-making over model complexity.

---

## Business Problem
Customer churn directly impacts bank profitability, acquisition costs, and long-term growth.  

**Objective:** Predict customer churn and identify key drivers so the bank can take proactive, targeted retention actions.

---

## Business Objectives
- Predict which customers are likely to churn
- Identify early churn risk signals
- Understand why customers churn (model explainability)
- Reduce churn through targeted interventions
- Support data-driven decision-making

---

##  Dataset Overview
- **Type:** Public, simulated real-world banking dataset  
- **Level:** Customer-level  
- **Rows:** 5,000 customers  
- **Target variable:** `churn` (1 = churned, 0 = retained)  

**Key Features:**  
- Credit score  
- Tenure  
- Number of products  
- Account balance  
- Activity status  
- Complaints in last 12 months  

---

## Exploratory Data Analysis (EDA)

### Churn Distribution

*Insight:* Dataset is highly imbalanced (~20% churn). Inactive or single-product customers have higher churn.

### Feature Insights
- Average Account Balance vs Churn  
- Number of Products vs Churn  
- Complaints vs Churn  

---

## Feature Engineering
- Created credit score bands  
- Encoded categorical variables  
- Scaled numerical features  
- Prepared data for machine learning models  

*Goal:* Improve predictive power and interpretability.

---

## Modeling & Evaluation

### Model Performance Comparison

| Model                 | ROC-AUC |
|-----------------------|---------|
| Logistic Regression   | 0.775   |
| Random Forest         | 0.758   |
| Gradient Boosting     | 0.759   |
| XGBoost               | 0.735   |

*Observation:* Logistic Regression outperformed ensemble models due to dataset size and linear relationships.

---

## Threshold Optimization

**Findings:**
- Maximum Recall occurs at threshold = 0.0 (trivial solution)  
- Best F1-score achieved at threshold = 0.535 (F1 = 0.364)  

*Insight:* Threshold adjustment is crucial for aligning model predictions with business retention objectives.

---

##  Model Explainability (SHAP)

**Top Drivers of Churn:**
- Low tenure  
- Low number of products  
- Inactivity  
- Recent complaints  
- Low account balance  

*Key insight:* Engagement and service experience drive churn more than demographics.

---

##  Business Insights (10 Critical Points)
1. New customers churn at higher rates  
2. Single-product customers are most vulnerable  
3. Inactivity is a strong churn signal  
4. Complaints are early churn warnings  
5. Low account balances correlate with churn  
6. Multi-product customers are more loyal  
7. Engagement matters more than age or gender  
8. Early intervention reduces churn risk  
9. Churn prediction enables proactive retention  
10. Explainable models are essential for compliance  

---

## Business Recommendations
- Strengthen onboarding for new customers  
- Launch cross-sell campaigns early  
- Trigger retention actions after first complaint  
- Reactivate inactive customers with incentives  
- Prioritize explainable ML models for compliance  

---

## Notebooks
- [01_eda.ipynb](notebooks/01_eda.ipynb)  
- [02_feature_engineering.ipynb](notebooks/01_feature_engineering.ipynb)  
- [03_modeling.ipynb](notebooks/01_modeling.ipynb)  
- [04_shap_explainability.ipynb](notebooks/01_shap_explainability.ipynb)  

---

## Tools & Technologies
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- SHAP  

---

##  How This Project Adds Business Value
- Reduces customer acquisition costs  
- Improves customer lifetime value  
- Enables explainable, compliant ML decisions  
- Translates data into actionable strategy  

---

## Author

Nhlanhla Lekgale  
Data Science | Machine Learning | Python | Business-Focused AI
