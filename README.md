# 🏡 California Housing Value Prediction

## 📋 Overview

This project predicts the median housing values in California districts using data from the 1990 U.S. Census. Various machine learning models, including regression and ensemble methods, were developed and evaluated to determine the most effective approach for this dataset.

## 📄 Dataset

The dataset provides information on houses in California districts and summary statistics based on the 1990 census. Each row corresponds to a census block group, the smallest geographical unit for which the U.S. Census Bureau publishes data.

🔗 **[Download the dataset](https://github.com/ageron/handson-ml/tree/master/datasets/housing)**

### Columns

1. **`longitude`**: Longitude of the block group.
2. **`latitude`**: Latitude of the block group.
3. **`housing_median_age`**: Median age of houses in the block group.
4. **`total_rooms`**: Total number of rooms in the block group.
5. **`total_bedrooms`**: Total number of bedrooms in the block group.
6. **`population`**: Total population in the block group.
7. **`households`**: Total number of households in the block group.
8. **`median_income`**: Median income of households in the block group (in tens of thousands of dollars).
9. **`median_house_value`**: Median house value in the block group (in dollars).
10. **`ocean_proximity`**: Proximity of the block group to the ocean.

## 🎯 Objective

To explore and process the dataset, develop regression models to predict the median housing value, train machine learning algorithms, and evaluate their performance.

## 🔍 Exploratory Data Analysis (EDA)

### Key Findings

- **Missing Values**: `total_bedrooms` has 207 missing values, filled using the median.
- **Outliers**: Present in `total_bedrooms`, `median_house_value`, `median_income`, and `households`.
- **Correlations**: Strong correlation between `median_house_value` and `median_income`. High inter-correlation among `households`, `population`, `total_bedrooms`, and `total_rooms`.
- **Distribution**: Skewed distributions and broad ranges in `households`, `population`, `total_bedrooms`, `total_rooms`, and `median_income`.

### Visualizations

- **Histograms**: Highlight skewed data distributions and outliers.
- **Scatter Plots**: Show linear relationships between `median_house_value` and other features.
- **Box Plots**: Used to identify outliers and understand data distribution.

## 🛠️ Data Preparation

### Data Cleaning

1. **Handling Missing Values**: Filled missing `total_bedrooms` with median values.
2. **Removing Duplicates**: No duplicates found in the dataset.
3. **Handling Outliers**: Processed outliers in `median_house_value`, `median_income`, and `households`.

### Data Transformation

1. **Normalization**: Applied Min-Max scaling to numerical features to ensure consistent ranges.
2. **Encoding Categorical Variables**: Converted `ocean_proximity` into numerical values using label encoding.

## 🤖 Machine Learning Models

### 1. Multiple Linear Regression (MLR)

**Description**: Models the relationship between a dependent variable and multiple independent variables with a linear equation.

**Performance**:
- **Training R²**: 0.592
- **Testing R²**: 0.599
- **MSE**: $3,555,499,321
- **RMSE**: $59,628
- **MAE**: $44,844
- **Adjusted R²**: 0.598
- **MAPE**: 28.56%

### 2. Decision Tree Regression

**Description**: Splits data into subsets based on feature values to capture non-linear relationships.

**Performance**:
- **Training R²**: 0.761
- **Testing R²**: 0.644
- **MSE**: $3,158,258,573
- **RMSE**: $56,198
- **MAE**: $38,505
- **Adjusted R²**: 0.643
- **MAPE**: 22.47%

### 3. Bagging Regressor

**Description**: Combines predictions from multiple decision trees to improve accuracy.

**Performance**:
- **Training R²**: 0.807
- **Testing R²**: 0.731
- **MSE**: $2,383,877,724
- **RMSE**: $48,825
- **MAE**: $34,073
- **Adjusted R²**: 0.731
- **MAPE**: 20.29%

### 4. AdaBoost Regressor

**Description**: Sequentially applies weak learners, focusing on correcting errors made by previous models.

**Performance**:
- **Training R²**: 0.854
- **Testing R²**: 0.747
- **MSE**: $2,245,030,115
- **RMSE**: $47,382
- **MAE**: $36,895
- **Adjusted R²**: 0.746
- **MAPE**: 25.35%

### 5. Random Forest Regression

**Description**: Constructs multiple decision trees and aggregates their predictions for improved accuracy.

**Performance**:
- **Training R²**: 0.965
- **Testing R²**: 0.772
- **MSE**: $2,021,954,958
- **RMSE**: $44,966
- **MAE**: $30,222
- **Adjusted R²**: 0.772
- **MAPE**: 17.62%

### Model Comparison

| Model                   | Training R² | Testing R² | MSE           | RMSE  | MAE    | Adjusted R² | MAPE   |
|-------------------------|-------------|------------|---------------|-------|--------|-------------|--------|
| Multiple Linear Regression | 0.592        | 0.599      | $3,555,499,321 | $59,628 | $44,844 | 0.598       | 28.56% |
| Decision Tree Regression   | 0.761        | 0.644      | $3,158,258,573 | $56,198 | $38,505 | 0.643       | 22.47% |
| Bagging Regressor          | 0.807        | 0.731      | $2,383,877,724 | $48,825 | $34,073 | 0.731       | 20.29% |
| AdaBoost Regressor         | 0.854        | 0.747      | $2,245,030,115 | $47,382 | $36,895 | 0.746       | 25.35% |
| Random Forest Regression   | 0.965        | 0.772      | $2,021,954,958 | $44,966 | $30,222 | 0.772       | 17.62% |

## 📊 Conclusions

- **Random Forest Regression** exhibited the best performance, excelling in prediction accuracy and generalizability.
- **AdaBoost Regressor** and **Bagging Regressor** also provided strong results, effectively handling complex patterns.
- **Decision Tree Regression** and **Multiple Linear Regression** offered simpler, interpretable models but were less accurate compared to ensemble methods.

Ensemble methods, especially Random Forest and AdaBoost, significantly improved prediction accuracy and effectively captured complex patterns in the data.



## 🔗 References

- [California Housing Data](https://github.com/ageron/handson-ml/tree/master/datasets/housing)
- [Kaggle Project Link](https://www.kaggle.com/code/mohamedabdelnasser/california-housing-eda-and-prices-prediction)
---

This README provides a comprehensive overview of the project, detailing the dataset, objectives, EDA findings, data preparation steps, model descriptions and evaluations, and overall conclusions.
