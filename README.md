Athlete Age Prediction
This project predicts the age of athletes based on their marathon performance data, specifically the time taken in the first and second splits, and their gender. The goal is to find the best machine learning model that provides the most accurate predictions.

Dataset
The dataset used for this project contains the following features:

First Half: Time taken in the first half of the marathon
Second Half: Time taken in the second half of the marathon
Gender: Gender of the athlete
Age: Age of the athlete (target variable)
Project Structure
Athletes.csv: The dataset file containing the athlete data.
AthletesAge.ipynb: The main script for data preprocessing, model training, and evaluation.


Libraries Used
pandas ,
scikit-learn ,
xgboost





STEPS
1. Data Preprocessing
a)Load the dataset and drop rows with missing values.
b)Extract relevant features (First Half, Second Half, Gender) and the target variable (Age).
c)Apply transformations using ColumnTransformer:
d)Standardize numerical features (First Half, Second Half).
e)One-hot encode the categorical feature (Gender).


2. Train-Test Split
Split the data into training and test sets (80% training, 20% testing).




4. Model Training
Define a set of models and their hyperparameters for tuning:
Ridge Regression ,
Lasso Regression ,  
Random Forest Regressor ,
Gradient Boosting Regressor ,
XGBoost Regressor ,
Performing grid search cross-validation to find the best hyperparameters for each model based on Mean Absolute Error (MAE) .
Selecting the best model based on the lowest MAE.



5. Model Evaluation
a)Training the best model on the entire training set.
b)Making predictions on the test set.
c)Calculating and print the evaluation metrics:
d)Mean Absolute Error (MAE)
e)Mean Squared Error (MSE)
f)Root Mean Squared Error (RMSE)
g)R-squared (R²)
h)R-squared as a percentage




6. Display Results
Print the best model's name and its evaluation metrics.
Display a few sample predictions along with the actual ages.
