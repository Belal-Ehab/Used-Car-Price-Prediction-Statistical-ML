# Used Car Price Prediction Using Statistical and Machine Learning Models

## Overview
This project focuses on predicting **used car prices** using a combination of statistical analysis, feature engineering, and machine learning regression models. Multiple modelling strategies are evaluated to analyse bias–variance trade-offs and identify the most robust predictors of car prices.

The project was developed as part of a **Machine Learning and Statistical Analysis Course** and emphasises data cleaning, exploratory data analysis, feature selection, outlier handling, and model generalisation.

---

## Dataset
The dataset was sourced from Kaggle:

**Used Cars Price Prediction**  
Author: Avikas Liwal  
Source: https://www.kaggle.com/datasets/avikasliwal/used-cars-price-prediction

Files used:
- `train-data.csv`
- `test-data.csv`

> Raw dataset files are **not included** in this repository due to dataset licensing and size considerations.

---

## Data Cleaning & Preprocessing
Key preprocessing steps included:
- Extraction of numeric values from string-based features (Engine, Power, New Price)
- Handling missing values using statistically appropriate methods (mean/median based on skewness)
- Brand-based imputation for missing prices and seats
- Encoding of categorical variables
- Removal of non-informative features
- Outlier treatment using **IQR-based clipping**

---

## Exploratory Data Analysis (EDA)
EDA was conducted to understand:
- Price distribution and skewness
- Relationship between price and key features (year, kilometers driven, engine power)
- Feature correlations with the target variable
- Feature-to-feature correlations to assess multicollinearity

---

## Feature Selection Strategies
Two feature selection approaches were evaluated:
1. **Manual Feature Selection** based on domain knowledge and correlation analysis
2. **Automated Feature Selection** using ANOVA F-tests (`SelectKBest`)

Both strategies were tested on:
- Original (unclipped) data
- Outlier-clipped data

---

## Models Evaluated
The following regression models were implemented and tuned:
- Linear Regression
- Polynomial Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

Hyperparameter tuning was performed using **GridSearchCV**.

---

## Evaluation Metrics
Models were evaluated using:
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R-squared (R²)
- Training time

Performance was compared across:
- Validation sets
- Test sets
- Feature selection methods
- Clipped vs unclipped data

---

## Final Results
Outlier clipping and feature engineering significantly improved model generalisation.

**Best performing model:**  
**Gradient Boosting Regressor**

Performance:
- Validation RMSE: **2.1133**
- Validation R²: **0.9304**
- Test RMSE: **1.6756**
- Test R²: **0.9508**

The close alignment between validation and test metrics indicates strong generalisation with no evidence of overfitting.

---

## Repository Structure
- Used_Car_Price_Prediction_Statistical_ML.ipynb
- LICENSE
- README.md

---

## Contributors
This project was completed as a **group project**.

- **Belal Ehab**
- **Khadija Wesam**
- **Lama Nezar**
- **Zeinab Mohamed**

---

## License
This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.

---

## Author
**Belal Ehab**  
Machine Learning and Statistical Analysis Project  
2026
