# MSCS_634_ProjectDeliverable_2

## Dataset Summary

- **Dataset Name**: Heart Disease UCI
- **Source**: [Kaggle] https://www.kaggle.com/datasets/ineubytes/heart-disease-dataset
- **Records**: 1026
- **Attributes**: 14 (including target)
- **Objective**: Predict the presence (1) or absence (0) of heart disease based on features like age, sex, cholesterol, resting blood pressure, maximum heart rate, and more.

## Dataset Description
The dataset includes patient health records with variables such as age, sex, chest pain type (cp), blood pressure (trestbps), cholesterol (chol), fasting blood sugar (fbs), maximum heart rate (thalach), and more. The target variable indicates the presence of heart disease (1) or absence (0).

## Modeling Process
I performed feature engineering by encoding categorical variables and applied three regression models:
- **Linear Regression**
- **Ridge Regression** (α = 1.0)
- **Lasso Regression** (α = 0.1)

I trained each model using an 80-20 train-test split and evaluated them with RMSE and R². I also applied 5-fold cross-validation to assess model generalizability.

## Results Summary

| Model   | RMSE     | R²       | CV Mean R²  |
|---------|----------|----------|-------------|
| Linear  | 0.377366 | 0.430367 | 0.517773    |
| Ridge   | 0.374593 | 0.438707 | 0.519397    |
| Lasso   | 0.446029 | 0.204212 | 0.268160    |


## Key Observations
- Ridge Regression outperformed the other models slightly in both test R² and cross-validation, indicating improved generalization and reduced overfitting.
- Linear Regression performed well but lacked regularization, which might affect stability on unseen data.
- Lasso Regression underperformed, likely due to excessive regularization (possibly setting key feature coefficients to zero), which led to underfitting.

## Challenges
- Tuning the alpha hyperparameter for Ridge and Lasso was critical to balancing bias and variance.
- With a relatively small dataset, ensuring stable cross-validation results was important to avoid misleading model performance.
- Managing feature selection and encoding appropriately had a noticeable impact on model accuracy.


## Author
Pawan Pandey  
Advanced Big Data and Data Mining (MSCS-634-B01)  
University of the Cumberlands  