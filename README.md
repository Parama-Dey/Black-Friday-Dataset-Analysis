# Black-Friday-Dataset-Analysis
A data science project analyzing Black Friday purchase behavior with EDA, feature engineering, outlier imputation, and recommendation systems.

## 📌 Project Overview
This project analyzes Black Friday purchase behavior using advanced **data cleaning, exploratory data analysis (EDA), feature engineering, outlier handling, and recommendation systems**.  
The goal is to uncover customer insights, improve predictive modeling, and build personalized product recommendations.
## Notebook Structure:
## 1.Importing Necessary Libraries

## 2.Importing The Dataset
---

## 3. Data Cleaning and Preprocessing
- Removed duplicate entries and standardized column formats.
- Converted categorical variables (e.g., `Gender`, `Age`, `City_Category`) into consistent formats.
- Handled special characters (e.g., `Stay_In_Current_City_Years` with “+” values).
- Ensured numeric columns were properly typed for analysis.

---

## 4. Initial Analysis
- Inspected dataset shape, column types, and basic statistics.
- Identified key variables: `User_ID`, `Product_ID`, `Purchase`, and product categories.
- Observed skewness in purchase values and sparsity in product interactions.

---

## 5. Identifying Missing Values in the Dataset
- Checked for nulls in product category columns (`Product_Category_2`, `Product_Category_3`).
- Applied imputation strategies:
  - Winsorization (capping extreme values).
  - Group-based imputation (by occupation or product category).
  - Log transformation for skewed distributions.

---

## 6. EDA - Univariate Analysis of Numerical Variables
- Histograms and violin plots for `Purchase`, `Rolling_Purchase`, `Occ_Mean_Purchase`, etc.
- Identified outliers and distribution patterns.

---

## 7. EDA - Univariate Analysis of Categorical Variables
- Count plots for `Gender`, `Age`, `Occupation`, `City_Category`, `Marital_Status`.
- Observed imbalances (e.g., more male shoppers, certain age groups dominating).

---

## 8. Bivariate Analysis
- Explored relationships between product categories and purchase amounts.
- Transition probability heatmaps (Category 1 → Category 2).
- Identified strong cross-category purchase patterns.

---

## 9. Multivariate Analysis
- Combined demographic and behavioral features.
- Detected interaction effects (e.g., Age × Occupation, City × Tenure).

---

## 10. Correlation Matrix
- Heatmap of numeric features.
- Found strong negative correlation between `Product_Category_1` and `Purchase`.
- Positive correlation between `Product_Category_3` and `Purchase`.

---

## 11. Outlier Analysis
- Boxplots before and after imputation.
- Compared median replacement vs. winsorization vs. group-based imputation.
- Stabilized skewed purchase distributions.

---

## 12. Feature Engineering

### 12.A Creation of New Features
- **Customer-level**: Total spend, average spend, transaction count, category diversity.
- **Product-level**: Popularity, average purchase value.
- **Interaction features**: Age × Occupation, City × Tenure, High Value Flag.
- **Behavioral features**: Rolling purchase trends, category-switch counts.

### 12.B Visualization of Feature Importance Scores (New vs Old)
- Compared raw vs engineered features using model importance scores.
- Engineered features (Rolling_Purchase, Age_Occupation, City_Tenure) ranked higher than raw demographics.

### 12.C Violin Plots and Histograms of New Features
- Visualized distributions of engineered features.
- Highlighted differences before and after imputation.

---

## 13. User Recommendation
- Built a **user–product interaction matrix**.
- Applied collaborative filtering and latent factor models (SVD).
- Generated personalized product recommendations:
  - Example: User 1000001 → Top 5 recommended products with scores.
- Integrated category transition probabilities for next likely purchase categories.

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/blackfriday-customer-insights-recommender.git
