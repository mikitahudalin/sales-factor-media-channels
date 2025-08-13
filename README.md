
# Advertising Spend Analysis & Sales Prediction

## 📌 Overview

This notebook analyzes the relationship between advertising spend across different media channels (TV, Radio, and Newspaper) and sales performance using **Linear Regression**.
The analysis explores both single-variable and multi-variable regression models to identify which channels significantly contribute to predicting sales.

Dataset: `advertising.csv`

---

## 📂 Contents

1. **Data Loading & Exploration**

   - Load the advertising dataset.
   - Generate descriptive statistics.
   - Use pairplots to visually explore relationships between sales and ad spending in each medium.
2. **Model Building & Evaluation**

   - **Model 1:** `sales ~ TV`Examines the effect of TV ad spend on sales.
   - **Model 2:** `sales ~ radio`Examines the effect of Radio ad spend on sales.
   - **Model 3:** `sales ~ TV + radio`Combines TV and Radio to assess combined impact.
   - **Model 4:** `sales ~ TV + radio + newspaper`
     Tests if adding Newspaper improves the model.
3. **Model Comparison & Insights**

   - R-squared and Adjusted R-squared comparisons.
   - Statistical significance of coefficients.
   - Residual analysis and normality checks.

---

## 📊 Key Findings

### **Model 1: TV Only**

- **R²:** 0.612 → TV ad spend explains ~61% of sales variance.
- **Effect:** +0.0475 sales per unit increase in TV spend.
- **Significance:** Statistically significant (p < 0.05).

### **Model 2: Radio Only**

- **R²:** 0.332 → Radio ad spend explains ~33% of sales variance.
- **Effect:** +0.2025 sales per unit increase in Radio spend.
- **Significance:** Statistically significant (p < 0.05).
- **Note:** Residuals deviate from normal distribution.

### **Model 3: TV + Radio**

- **R²:** 0.897 → 89.7% of sales variance explained.
- **Both TV and Radio:** Significant predictors (p < 0.05).
- **Improvement:** Large jump in explanatory power compared to single-variable models.
- **Note:** Residuals still deviate from normality.

### **Model 4: TV + Radio + Newspaper**

- **R²:** No improvement over Model 3.
- **Newspaper coefficient:** Not statistically significant (p = 0.860).
- **Conclusion:** Newspaper ads add no predictive value when TV and Radio are already included.

---

## 📈 Conclusion

- **Best Model:** `sales ~ TV + radio`Offers strong explanatory power and simplicity.
- **Newspaper advertising** does not significantly impact sales when TV and Radio are accounted for.
- **Recommendation:** Focus budget on TV and Radio for higher sales impact.

---

## ⚙️ Requirements

- Python 3.x
- pandas
- matplotlib
- seaborn
- statsmodels
- gdown (for dataset download)

---

Investigating impact of investitions in different media channels on sales
