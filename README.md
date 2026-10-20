# Customer Churn Prediction and Retention Analytics

**Tools:** Python, Pandas, NumPy, scikit-learn, SQL, SciPy, Matplotlib, Seaborn

## 1. Business Problem

Customer churn reduces recurring revenue and increases customer acquisition costs. The objective of this project is to identify customers at elevated risk of leaving, understand churn patterns, segment customers into actionable groups, and propose evidence-based retention strategies.

## 2. Analytical Approach

- Conducted exploratory data analysis and data-quality checks.
- Used SQL to analyze churn across contract types and tenure groups.
- Applied a chi-square test of independence and Cramér's V to examine the association between contract type and churn.
- Compared Logistic Regression, Decision Tree and Random Forest using five-fold cross-validation and held-out test evaluation.
- Applied K-Means clustering and evaluated candidate cluster counts using inertia and silhouette scores.
- Combined customer segments with predicted churn probabilities to identify retention priorities.

## 3. Predictive Model Results

Random Forest was selected for the retention-focused analysis.

- Test ROC-AUC: 0.8422
- Test recall: 75.40%
- Test precision: 53.92%
- Test F1-score: 0.6288
- True positives: 282
- False negatives: 92
- False positives: 241

The model identified more actual churners than Logistic Regression, but it also generated more false positives. This trade-off should be assessed against intervention costs and outreach capacity.

## 4. Statistical Findings

Contract type was significantly associated with churn (chi-square statistic = 1184.5966, degrees of freedom = 2, p-value = 5.86304 × 10⁻²⁵⁸). Cramér's V was 0.4101.

Observed churn rates were 42.71% for month-to-month contracts, 11.27% for one-year contracts and 2.83% for two-year contracts.

Churn also declined across the analyzed tenure groups, from 47.44% among customers with up to 12 months of tenure to 11.93% among customers with 37 or more months.

These are observational associations and do not establish causality.

## 5. Customer Segmentation

A four-cluster K-Means solution was retained provisionally for business interpretation. Its silhouette score was 0.4722, compared with 0.4797 for two clusters.

The four-cluster solution identified a segment with an observed churn rate of 48.24%, characterized by relatively short tenure, higher average monthly charges, a high proportion of month-to-month contracts and substantial fiber-optic internet usage.

A lower-churn segment had an observed churn rate of 5.00% and a higher proportion of two-year contracts.

## 6. Business Recommendations

1. Investigate early-life churn among month-to-month customers.
2. Examine service value, support needs and billing experience in the highest-churn segment.
3. Prioritize outreach using predicted risk while accounting for false positives and available capacity.
4. Test targeted retention interventions using a controlled experiment.
5. Monitor recall, precision, ROC-AUC, calibration and business outcomes over time.

## 7. Limitations and Next Steps

Model predictions do not guarantee customer behaviour or intervention success. Cluster characteristics and statistical associations do not establish causal explanations.

Next steps include threshold and cost analysis, permutation feature importance, cluster stability assessment, probability calibration, and experimental validation of retention interventions.
