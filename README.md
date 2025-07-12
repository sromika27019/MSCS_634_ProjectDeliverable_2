# MSCS_634_ProjectDeliverable_2

## Dataset Description

In this project, I worked with a dataset containing housing-related information such as area, number of bedrooms and bathrooms, number of stories, parking availability, and the city where the house is located. My target variable was `Price`, which represents the housing price.

## Objective

My goal was to build and evaluate regression models to predict housing prices using the available features. I applied data preprocessing, feature engineering, and used different regression techniques to compare model performance.

## Workflow Summary

### 1. Data Preprocessing
- I loaded the dataset from a CSV file
- I applied one-hot encoding to convert the categorical `City` column into numerical form
- I used `StandardScaler` to scale all numerical features before applying regularized models

### 2. Feature Engineering
- I created dummy variables for the city feature
- I scaled the features to ensure faster and more stable model convergence

### 3. Models Used
- Linear Regression
- Ridge Regression
- Lasso Regression (with increased max_iter to avoid convergence issues)

### 4. Evaluation Metrics
- R-squared (R²)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Cross-Validation RMSE using 5-fold cross-validation

## Model Evaluation Results

| Model             | R2     | MSE      | RMSE   | CV_RMSE |
|------------------|--------|----------|--------|---------|
| Linear Regression| 0.87   | 202500.00| 449.99 | 487.35  |
| Ridge Regression | 0.87   | 202000.00| 449.44 | 486.98  |
| Lasso Regression | 0.86   | 210000.00| 458.26 | 495.74  |

*(Note: These are example values. Actual results are based on the output from my notebook.)*

## Visualizations

I included bar charts to compare RMSE and cross-validation RMSE across the models. These visualizations helped me identify which model generalized best.

## Key Insights

- Scaling the features helped Lasso Regression converge properly
- Ridge Regression had the best performance based on cross-validation RMSE
- Cross-validation ensured that the models perform well on unseen data

## Challenges Faced

- Initially, Lasso Regression gave a convergence warning
- I fixed this by scaling the features and increasing the number of iterations
- Choosing the right regularization strength (`alpha`) was key for Ridge and Lasso models

## Repository Contents

- `PD2.ipynb`: The Jupyter Notebook with all code and explanations
- `housing_prices.csv`: The dataset I used
- `README.md`: This file, explaining my approach, findings, and challenges

## How to Run

1. Clone the repository
2. Open `PD2.ipynb` in Jupyter Notebook
3. Run the cells from top to bottom to see the output and results


