# Fuel Cell Performance Prediction

This project aims to predict the performance of fuel cells using various machine learning models and preprocessing configurations. The models were evaluated using multiple metrics to identify the best-performing model.

## Model Comparison

We experimented with multiple configurations, training models under different combinations of the following preprocessing conditions:

1. **Preprocessing**: Enabled or Disabled (handling missing values, encoding, etc.)
2. **Data Split Shuffle**: Whether to shuffle the dataset before splitting into training and test sets.
3. **Normalization**: Whether to normalize the data (Z-score normalization).
4. **Feature Selection**: Whether to perform feature selection (removing irrelevant features).
5. **Remove Outliers**: Whether to remove outliers from the dataset.

### Configurations Compared

| **Configuration** | **Preprocessing** | **Data Split Shuffle** | **Normalize** | **Feature Selection** | **Remove Outliers** |
|--------------------|-------------------|-------------------------|---------------|------------------------|----------------------|
| Config 1           | False            | False                  | False         | False                 | False               |
| Config 2           | False            | True                   | False         | False                 | False               |
| Config 3           | True             | True                   | False         | False                 | False               |
| Config 4           | True             | True                   | True          | False                 | False               |
| Config 5           | True             | True                   | True          | True                  | False               |
| Config 6           | True             | True                   | True          | True                  | True                |
| Config 7           | True             | True                   | False         | True                  | False               |
| Config 8           | False            | True                   | True          | False                 | True                |

## Model Evaluation

Each model was evaluated using the following performance metrics:

- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**
- **R² (Coefficient of Determination)**
- **RMSLE (Root Mean Squared Logarithmic Error)**
- **MAPE (Mean Absolute Percentage Error)**
- **Time Taken (TT)**

## Best Performing Model

After comparing all models, the best-performing model was identified as follows:

### Extra Trees Regressor

| **Metric**       | **Value**      |
|------------------|----------------|
| **MAE**          | 4.94           |
| **MSE**          | 55.877         |
| **RMSE**         | 7.312          |
| **R²**           | 0.971          |
| **RMSLE**        | 0.137          |
| **MAPE**         | 0.114          |
| **Time Taken**   | 0.201 seconds  |

## Conclusion

By comparing the models with different configurations, the best-performing model is **Extra Trees Regressor** with an **R² value of 0.971**, indicating high accuracy in predictions.
