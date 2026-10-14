# Bank Customer Churn — EDA & ML Error Analysis

## Overview

This project explores a bank customer churn dataset from Kaggle through Exploratory Data Analysis (EDA) and machine learning error analysis.

The analysis investigates relationships between customer characteristics and churn behavior, examines patterns associated with higher churn rates, and identifies customer groups that a predictive model frequently misclassifies. By analyzing prediction errors, particularly false negatives, this project aims to understand which customer characteristics may be overlooked by the model and identify opportunities for feature engineering and model improvement.

## Objectives

- Explore customer demographics, account characteristics, and behavioral features.
- Identify patterns and characteristics associated with customer churn.
- Investigate relationships between features and churn rates.
- Evaluate model performance using classification metrics.
- Analyze misclassified customers, especially customers who churned but were predicted not to churn.
- Identify potential opportunities for feature engineering and model improvement.

## Key Findings

### 1. Geographical Differences

Churn patterns differ across geographical regions. Germany has a higher churn rate than France despite having a smaller customer population. This suggests that geographical information may help distinguish customer churn patterns.

### 2. Age and Churn

Older customers generally exhibit higher churn rates in this dataset. Age-based feature engineering may help the model capture differences in churn behavior across customer age groups.

### 3. Account Balance

Customers with positive account balances show different churn patterns from customers with zero balances. Further analysis also reveals geographical differences in account balance distributions, particularly among German customers.

### 4. Customer Activity

Inactive members tend to have higher churn rates than active members. Customer activity may therefore provide useful information for distinguishing customers with different churn risks.

### 5. Number of Products

Customers with three or four products exhibit unusually high churn rates. However, these groups contain relatively few observations, so the findings should be interpreted cautiously.

### 6. Class Imbalance

Churners represent a minority of the dataset. This class imbalance can affect model performance, particularly its ability to identify customers who will churn.

## Machine Learning Error Analysis

Beyond evaluating overall model performance, this project examines the characteristics of misclassified customers.

The analysis investigates false negatives: customers who actually churned but were predicted by the model as non-churners.

Key areas of investigation include:

- Age groups and geographical regions associated with missed churn predictions.
- The role of customer activity in prediction errors.
- Whether combinations of customer characteristics reveal patterns that individual features do not capture.
- Whether feature engineering can help the model recognize customer groups that it frequently misclassifies.

These findings help identify potential weaknesses in the model and guide further experimentation.

## Methodology

1. Data inspection and exploratory data analysis.
2. Analysis of customer characteristics and churn rates.
3. Feature engineering, including grouping selected numerical variables.
4. Model training and evaluation using classification metrics.
5. Hyperparameter and classification-threshold experimentation.
6. Error analysis to investigate false negatives and other misclassifications.

## Limitations

- The analysis identifies associations, not causal relationships.
- High churn rates in small customer groups may be unstable.
- Model performance depends on the dataset, selected features, validation strategy, and classification threshold.
- Error analysis can reveal patterns in misclassified customers, but it does not establish why the model makes those errors.
- Findings from this dataset may not generalize to other banks or customer populations.

## Tools and Technologies

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- XGBoost
- Jupyter Notebook

## Project Structure

```text
Bank-Churn-EDA-ML-Analysis/
├── Model/
│   ├── Customer-Churn-Records.csv
│   └── Data.ipynb
└── README.md
```

## Conclusion

This project combines exploratory data analysis with machine learning error analysis to investigate bank customer churn from both a data and model-performance perspective.

Rather than focusing only on overall predictive performance, the analysis examines customer characteristics associated with churn and investigates groups that the model struggles to identify. These insights provide a foundation for more targeted feature engineering, improved evaluation, and future churn prediction experiments.