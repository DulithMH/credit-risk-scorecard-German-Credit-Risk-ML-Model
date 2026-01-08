# 💰 Credit Risk Scorecard System

## 📌 Project Overview
Built a regulatory-compliant **Credit Scoring Model** using the German Credit dataset. 
Unlike "Black Box" machine learning models, this project uses **Logistic Regression** to ensure full explainability (Glass Box), which is required by banking regulations (Basel Accords).

## 📊 Key Features
* **Risk Drivers:** Identified that customers with *no checking account* (A14) are 80% less likely to default than those with negative balances.
* **Assumptions Checked:** Verified Model Linearity, Multicollinearity (VIF < 5), and Independence (Durbin-Watson ~2.0).
* **Scorecard Scaling:** Converted raw probabilities into a standard **300-850 Credit Score**.

## 🛠️ Tech Stack
* **Python** (Pandas, Scikit-Learn, Statsmodels)
* **Statistical Tests:** VIF, WoE (Weight of Evidence), Durbin-Watson
* **Visualization:** Seaborn, Matplotlib

## 🚀 Results
* **ROC-AUC Score:** ~0.78 (Strong predictive power)
* **Differentiation:** Clear separation between "Good" (Avg Score: 750) and "Bad" (Avg Score: 520) customers.
