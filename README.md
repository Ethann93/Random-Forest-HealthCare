# Random Forest Regressor for Life Expectancy Prediction

This project focuses on predicting life expectancy using a Random Forest Regressor model. We will walk through the entire process from loading the dataset to model evaluation. The dataset used for this project is the 'healthexp' dataset from the Seaborn library, and our goal is to build a regression model that can accurately predict life expectancy.

## Dataset Exploration

We start by loading and exploring the 'healthexp' dataset:

- The dataset is loaded from the Seaborn library, and its structure and data types are inspected.

- Missing values are checked, ensuring the dataset is clean and ready for modeling.

## Model Preparation

Next, we prepare the data for modeling:

- We create binary numbers for categorical columns using one-hot encoding, making the data suitable for regression.

- We split the dataset into features (X) and the target variable (y).

- The data is further divided into training and testing sets, with 80% of the data used for training and 20% for testing.

## Random Forest Regressor Model

We use the Random Forest Regressor to predict life expectancy:

- We initialize a Random Forest Regressor model with a random seed for reproducibility.

- The model is trained on the training data (X_train and y_train).

- We make predictions on the test data (X_test).

## Initial Model Evaluation

We evaluate the initial Random Forest Regressor model using three performance metrics:

1. Mean Absolute Error (MAE): Lower values are better, indicating a smaller average absolute difference between predicted and actual values.

2. Mean Squared Error (MSE): Lower values are better, indicating a smaller average squared difference between predicted and actual values.

3. R-squared (R^2) Score: Higher values are better, indicating how well the model explains the variation in the target variable.

The initial model results are as follows:

- MAE: 0.2799
- MSE: 0.129
- R^2: 0.9893

The Random Forest model already performs well, but we aim to improve it further through hyperparameter tuning.

## Hyperparameter Tuning

We perform hyperparameter tuning using GridSearchCV to find the best set of hyperparameters for the Random Forest Regressor:

- A parameter grid is defined, specifying different values for hyperparameters like the number of estimators, max depth, and minimum samples for splitting and leaf nodes.

- GridSearchCV is employed to perform an exhaustive search for the best hyperparameters, optimizing for the negative mean squared error.

- The best hyperparameters are found, and the model is refit with these optimal parameters.

## Tuned Model Evaluation

After hyperparameter tuning, we evaluate the model again to check for improvements. The performance metrics are re-calculated:

- MAE: 0.2725
- MSE: 0.1211
- R^2: 0.9900

With hyperparameter tuning, the model results show slight improvements, demonstrating the effectiveness of the Random Forest Regressor for predicting life expectancy.

To further enhance the model's performance, additional steps can be considered, such as implementing cross-validation, exploring ensemble methods, and expanding the dataset if more data becomes available.

In summary, this project showcases the development and fine-tuning of a Random Forest Regressor model for predicting life expectancy. The model performs well, and with continuous optimization, it can be a valuable tool for life expectancy prediction.
