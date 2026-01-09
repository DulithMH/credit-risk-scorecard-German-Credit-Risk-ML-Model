Project Title: Credit Risk Prediction using Logistic Regression
1. Project Overview
Objective: Built a Machine Learning model to predict the probability of a customer defaulting on a loan.

Goal: Minimize financial loss by identifying high-risk applicants (prioritizing Recall).

Context: Internship Project for [Department Name] / University Assignment.

2. Data Processing Pipeline (The "How")
Data Cleaning: Handled missing values (Median imputation) and capped outliers (99th percentile) to reduce noise.

Feature Engineering:

Checked Linearity (Box-Tidwell) and applied Log transformations where necessary.

Verified Multicollinearity using VIF (Variance Inflation Factor) to remove redundant features.

Data Splitting: strictly separated Train/Test sets to prevent Data Leakage.

Scaling: Applied StandardScaler (fit on Train, transform on Test) to normalize features.

Handling Imbalance: Addressed the 70/30 class imbalance using SMOTE (Synthetic Minority Over-sampling Technique) on the Training set only.

3. Model Performance (The "Results")
Algorithm: Logistic Regression (optimized with max_iter=1000).

Threshold Tuning: Adjusted decision threshold from default 0.50 to 0.42 using the ROC-AUC Curve to maximize safety.

Key Metrics (Test Set):

Recall (Risk Detection): ~79% (Successfully identified most defaulters).

Precision: ~50% (Accepted a higher False Alarm rate to ensure safety).

AUC Score: [Insert your AUC Score, e.g., 0.76].

4. Business Insights (Interpretation)
Top Risk Drivers (+):

High Debt Ratio: Customers with higher debt loads are significantly riskier (Odds Ratio: 2.3x).

Recent Delinquencies: Past late payments are a strong predictor of future default.

Top Safety Indicators (-):

Annual Income: Higher income serves as a protective factor against default.

Credit History Length: Long-term customers show lower risk probabilities.

5. Technologies Used
Language: Python 3.x

Libraries:

Scikit-Learn (Modeling, Metrics, Scaling)

Imbalanced-Learn (SMOTE)

Pandas & NumPy (Data Manipulation)

Seaborn & Matplotlib (Visualization: Heatmaps, ROC Curve)

Statsmodels (Statistical Testing)



### 📊 Visuals

#### Confusion Matrix
![Confusion Matrix](images/confusion_matrix.png)

#### ROC Curve
![ROC Curve](images/roc_curve.png)
