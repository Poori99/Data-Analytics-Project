# Heart Failure Prediction Analysis

## Overview
This project analyzes the **[Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)** to identify key clinical and demographic factors influencing heart disease risk. The analysis includes data preprocessing, exploratory data analysis (EDA), statistical modeling, and clustering to provide actionable insights for preventive healthcare strategies.

## Dataset Description
- **Source**: [Kaggle](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- **Size**: 918 rows, 12 features
- **Features**:
  - **Clinical**: `RestingBP`, `Cholesterol`, `MaxHR`, `Oldpeak`, `FastingBS`, `ChestPainType`
  - **Demographic**: `Age`, `Sex`
  - **Target**: `HeartDisease` (1 = presence, 0 = absence)

## Methodology
### 1. Data Cleaning
- Removed invalid entries (e.g., `RestingBP = 0`, `Cholesterol = 0`).
- Encoded categorical variables (e.g., `Sex`, `ChestPainType`) using **one-hot encoding**.

### 2. Exploratory Data Analysis (EDA)
- **Summary statistics**: Analyzed distributions of key features like `Age` and `Cholesterol`.
- **Visualizations**:
  - Histograms and box plots for numerical features.
  - Bar charts for categorical variables.
  - Scatter plots and heatmaps to identify correlations.

### 3. Statistical Analysis
- **Logistic Regression**: Identified significant predictors of heart disease:
  - Top risk factors: `ST_Slope_Flat` (coefficient = +2.1), `ExerciseAngina_Y` (+1.8).
  - Protective factor: `MaxHR` (-0.03 per unit increase).
- **Clustering (K-means)**:
  - Segmented patients into 3 risk groups using features like `Age` and `Cholesterol`.
  - **High-risk cluster**: Older patients with elevated cholesterol and low MaxHR.

### 4. Tools & Libraries
- **Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`
- **Machine Learning**: `scikit-learn` (logistic regression, K-means)
- **Visualization**: `Plotly`, `PCA` for cluster visualization

## Key Findings
1. **Top Risk Factors**:
   - Abnormal ECG results (`ST_Slope_Flat`) and exercise-induced angina (`ExerciseAngina_Y`).
   - Low `MaxHR` and high `Oldpeak` (ST depression).
2. **Demographics**:
   - 72% of heart disease cases were male.
   - Median age of patients with heart disease: **58 years**.
3. **Clusters**:
   - **Cluster 1 (High Risk)**: Recommended for aggressive cholesterol management.
