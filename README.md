# Car Price Prediction using Supervised Machine Learning

## Project Title

Car Price Prediction using Linear Regression, Decision Tree, and Random Forest

## Objective

The objective of this project is to build supervised machine learning models to predict the selling price of a car based on various features such as year, fuel type, transmission type, and kilometers driven.
This project demonstrates the complete machine learning workflow including data preprocessing, model training, testing, and evaluation.


## Problem Statement

Car price prediction is an important task in the automobile market. The goal of this project is to develop regression models that can accurately estimate the selling price of a car using historical data and relevant features.

## Dataset Description

The dataset used in this project contains information about different cars and their selling prices.

### Dataset Features

 Column Name    -    Description                                      

 Car_Name      :  Name of the car                                  
 Year          : Manufacturing year of the car                    
 Selling_Price : Price at which the car is sold (Target Variable)
 Present_Price : Current showroom price                           
 Kms_Driven    : Total kilometers driven                          
 Fuel_Type     : Type of fuel used (Petrol/Diesel/CNG)            
 Seller_Type   : Type of seller (Dealer/Individual)               
 Transmission  : Transmission type (Manual/Automatic)             
 Owner         :  Number of previous owners                        

Target Variable: **Selling_Price**

## Data Preprocessing

Before applying machine learning algorithms, several preprocessing steps were performed to ensure data quality and improve model performance.

### 1. Handling Missing Values

The dataset was checked for missing values using `isnull()` function.
No missing values were found in the dataset.

### 2. Fixing Data Types

The dataset was inspected using `df.info()` to verify that all columns had correct data types for machine learning.

### 3. Removing Duplicate Records

Duplicate rows were removed using `drop_duplicates()` to avoid repeated observations affecting model training.

### 4. Detecting and Treating Outliers

Boxplots were used to visualize numerical columns and identify possible outliers that may affect model performance.

### 5. Handling Categorical Variables (Encoding)

Machine learning models require numerical input.
Categorical features such as:

* Fuel_Type
* Seller_Type
* Transmission

were converted into numerical format using **Label Encoding**.

### 6. Removing Irrelevant Features

The column **Car_Name** was removed because it does not contribute significantly to predicting the selling price.

### 7. Feature Scaling

Feature scaling was applied using **StandardScaler** to ensure that all numerical features are on a similar scale. This helps improve model performance.

### 8. Splitting the Dataset

The dataset was divided into **training and testing sets** using `train_test_split`.

* Training Data: 80%
* Testing Data: 20%

This helps evaluate the model's performance on unseen data.

## Machine Learning Algorithms Used

Three supervised regression algorithms were implemented:

### 1. Linear Regression

Linear Regression models the relationship between independent variables and the target variable using a linear equation.

### 2. Decision Tree Regressor

Decision Tree splits the dataset into multiple branches based on feature values and predicts numerical outcomes.

### 3. Random Forest Regressor

Random Forest is an ensemble learning method that combines multiple decision trees to produce more accurate and stable predictions.

## Evaluation Metrics

To evaluate the performance of the models, the following regression metrics were used:

### R² Score

Measures how well the model explains the variance in the target variable.

### Mean Squared Error (MSE)

Measures the average squared difference between predicted and actual values.

### Root Mean Squared Error (RMSE)

The square root of MSE which provides error in the same unit as the target variable.

### Mean Absolute Error (MAE)

Measures the average absolute difference between predicted and actual values.

## Model Results

After training and testing the models, their performance was compared using the evaluation metrics.

 Model               R² Score        MSE             RMSE             MAE           
  
 Linear Regression   0.741083      	6.673137      	2.583242	      1.541072,
 Decision Tree       0.790244	      5.406107	      2.325104	      1.118333 ,
 Random Forest       0.515198	      12.494917	      3.534815	      1.512017,


Replace the values with the results obtained from your notebook.

## Conclusion

This project implemented three supervised machine learning models to predict car selling prices.

Among the models tested, **Random Forest Regressor performed the best**, achieving the highest R² score and lowest prediction errors. This indicates that ensemble models can capture complex relationships in the data more effectively compared to simpler models.

The project demonstrates the importance of **data preprocessing, feature engineering, and model evaluation** in building reliable machine learning models.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
