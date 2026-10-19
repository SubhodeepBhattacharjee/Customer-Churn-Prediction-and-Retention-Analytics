# Customer Churn Prediction and Retention Analytics

## 1. Business Objective

The objective is to analyze customer churn patterns, identify customers at risk of leaving, and provide data-driven recommendations for improving customer retention.

## 2. Dataset

The project uses the IBM Telco Customer Churn dataset, containing customer demographics, subscription information, tenure, charges, services, and churn status.

## 3. Analytical Methodology

- Exploratory data analysis and data-quality checks.
- SQL-based analysis of churn by customer segment.
- Statistical hypothesis testing to investigate associations between contract type and churn.
- K-Means clustering to identify customer segments.
- Logistic regression, decision tree, and random forest model comparison.
- Cross-validation and held-out test-set evaluation.
- Customer risk ranking and illustrative retention-value analysis.

## 4. Selected Predictive Model

Random Forest is the selected model for the next stage of analysis. Its final suitability will be assessed using cross-validation, precision, recall, F1-score, ROC-AUC, and business requirements.

## 5. Business Insights

Document the observed churn rate, contract-level differences, customer segment profiles, and most informative model features using the actual analysis results.

## 6. Recommendations

Prioritize investigation of customer groups with elevated predicted churn risk. Design targeted retention experiments and measure their incremental impact before scaling interventions.

## 7. Limitations

Predicted probabilities are not guarantees of future behaviour. Observational associations do not establish causation. Model performance may change over time, and the business value of retention interventions requires separate evaluation.

## 8. Future Improvements

Evaluate threshold selection, calibration, permutation importance, model monitoring, and a controlled retention experiment.
