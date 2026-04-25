# 1. Project Title and Description.
Predicting individual medical charges using demographic, 
lifestyle and health features. Built using OLS regression 
with interaction terms and robust standard errors.
# 2. Dataset
Source: [Health Insurance Cost and Risk Dataset] (https://www.kaggle.com/datasets/mjawad17/health-insurance-cost-and-risk-dataset)
- 934 observations
- Target variable: Medical charges
# 3. Project Structure
├── Medical-charges_LinReg26A.ipynb  # Main analysis notebook
├── README.md
# 4. Key Findings
- BMI only affects charges for smokers — 
  alone it has no significant effect
- Age increases charges for everyone, but less so for smokers (net effect: +16 vs +22 for non-smokers)
  since smoking already has a high baseline cost.
-  Model struggles with non-smoker prediction (R²=39%) 
  suggesting missing health predictors for this group
# 5. Methodology
- OLS Regression with interaction terms
  (BMI×smoker, age×smoker)
- Square root transformation of charges 
  to address non-linearity
- HC3 robust standard errors to handle 
  remaining heteroscedasticity
- Standardized coefficients for feature importance ranking
- Overall R² = 0.848
# 6. Requirements
pandas
numpy
matplotlib
seaborn
statsmodels
scikit-learn
scipy
# 7. Limitations
- Non-smoker charges poorly predicted (R²=39%) 
  — likely missing health condition detail
- Children variable dominated by 0 children (61%) 
  limiting insight for large families
- Heteroscedasticity present but managed 
  via robust standard errors
