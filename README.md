# Predicting Bank Customer Churn and Identifying Key Driving Factors Using Machine Learning

## Overview

This project analyzes bank customers' demographic, financial, and behavioral data to predict customer churn and identify the key factors associated with customer attrition.

Several machine learning classification models were developed, evaluated, and compared, including both baseline and hyperparameter-tuned versions:

* Logistic Regression
* Decision Tree
* Random Forest
* XGBoost
* Random Forest (Tuned)
* XGBoost (Tuned)

Among all models, **XGBoost achieved the best overall performance**, reaching an Accuracy of **96.8%**, Precision of **90.4%**, Recall of **89.9%**, and an F1-Score of **90.1%**. Hyperparameter tuning produced only marginal changes, indicating that the original XGBoost model was already well optimized.

## Project Structure

```text
bank-churn-prediction/
│
├── data_loading.ipynb
├── exploratory_data_analysis.ipynb
├── modeling.ipynb
├── BankChurners.csv
├── requirements.txt
├── outputs/
└── README.md
```

## Installation and Execution

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run the notebooks in the following order:

1. data_loading.ipynb
2. exploratory_data_analysis.ipynb
3. modeling.ipynb

## Model Performance

| Model                 | Accuracy | Precision | Recall | F1-Score |
| --------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression   | 85.7%    | 54.0%     | 74.2%  | 62.5%    |
| Decision Tree         | 92.0%    | 69.9%     | 87.7%  | 77.8%    |
| Random Forest         | 95.4%    | 84.5%     | 87.1%  | 85.8%    |
| XGBoost               | 96.8%    | 90.4%     | 89.9%  | 90.1%    |
| Random Forest (Tuned) | 95.3%    | 84.4%     | 86.8%  | 85.6%    |
| XGBoost (Tuned)       | 96.8%    | 90.1%     | 89.9%  | 90.0%    |

## Key Findings

* The dataset exhibited a class imbalance (16% churn rate), which was addressed using SMOTE.
* Low transaction frequency (**Total_Trans_Ct**) was the strongest indicator of customer churn.
* Lower transaction amounts (**Total_Trans_Amt**) were associated with a higher churn risk.
* Low revolving balance (**Total_Revolving_Bal**) indicated lower customer engagement.
* Customers with more banking products (**Total_Relationship_Count**) were generally more loyal.
* A decline in transaction frequency over time (**Total_Ct_Chng_Q4_Q1**) served as an important early warning signal for churn.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* XGBoost
* Jupyter Notebook

## Dataset

The project uses the **Bank Customer Churn Dataset** obtained from Kaggle. The dataset contains approximately 10,000 customer records and includes demographic, financial, and behavioral features used to predict customer churn.
