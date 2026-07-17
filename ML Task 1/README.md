Customer Churn Prediction using Machine Learning
Project Overview

This project implements a Customer Churn Prediction System using the Random Forest Classification algorithm in Python. The objective is to predict whether a customer is likely to leave (churn) based on customer information such as credit score, geography, gender, age, balance, tenure, number of products, and other banking-related features.

The project follows the complete machine learning workflow, including data preprocessing, feature engineering, model training, prediction, and performance evaluation.

Objectives
Predict customer churn using supervised machine learning.
Perform data preprocessing and feature transformation.
Train a Random Forest Classifier.
Evaluate model performance using accuracy.
Visualize customer churn distribution.
Technologies Used
Python 3
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook
Dataset

The project uses the Churn_Modelling.csv dataset.

The dataset contains customer information such as:

Row Number
Customer ID
Surname
Credit Score
Geography
Gender
Age
Tenure
Balance
Number of Products
Has Credit Card
Is Active Member
Estimated Salary
Exited (Target Variable)

Target Variable

0 → Customer stays
1 → Customer leaves (Churn)
Machine Learning Workflow
Step 1: Import Libraries

Import the required Python libraries for data manipulation, visualization, preprocessing, model building, and evaluation.

Libraries used:

NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
Step 2: Load the Dataset

Load the Churn_Modelling.csv dataset using Pandas.

Example:

dataset = pd.read_csv("Churn_Modelling.csv")
Step 3: Explore the Dataset

Perform basic data analysis using:

dataset.head()
dataset.info()
dataset.describe()
dataset.isnull().sum()

This helps understand:

Number of rows
Number of columns
Data types
Missing values
Statistical summary
Step 4: Visualize Customer Churn

Create a count plot using Seaborn to visualize the number of customers who stayed and those who exited.

Visualization:

Customer Churn Distribution
Step 5: Data Preprocessing

Preprocess the dataset before training.

Operations performed:

Encode categorical variables
Convert text data into numerical format
Remove unnecessary columns
Separate input features and target variable

Removed columns:

RowNumber
CustomerId
Surname

Target:

Exited
Step 6: Feature Engineering

Categorical columns are transformed using:

Label Encoding
One-Hot Encoding

Columns encoded:

Geography
Gender
Step 7: Split the Dataset

Split the dataset into:

Training Dataset (80%)
Testing Dataset (20%)

Using:

train_test_split()
Step 8: Feature Scaling

Standardize numerical features using:

StandardScaler

This improves model performance by bringing all features to the same scale.

Step 9: Build the Machine Learning Model

Train the Random Forest Classifier using the training dataset.

Algorithm:

Random Forest Classifier

Advantages:

High accuracy
Handles large datasets
Reduces overfitting
Works well with mixed data
Step 10: Model Training

Train the classifier using:

model.fit(X_train, y_train)
Step 11: Prediction

Predict customer churn for the testing dataset.

y_pred = model.predict(X_test)
Step 12: Model Evaluation

Evaluate the model using:

Accuracy Score
accuracy_score(y_test, y_pred)
Project Process
Import required Python libraries.
Load the customer churn dataset.
Explore and inspect the dataset.
Check for missing values.
Visualize customer churn distribution.
Encode categorical variables.
Remove unnecessary columns.
Separate features and target variable.
Split the dataset into training and testing sets.
Standardize numerical features.
Train the Random Forest Classifier.
Predict customer churn on the test data.
Evaluate the model using accuracy.
Analyze the prediction results.

Output

The project produces:

Dataset information
Statistical summary
Customer churn distribution plot
Trained Random Forest model
Customer churn predictions
Model accuracy score

Advantages
Easy to understand implementation.
Fast training using Random Forest.
Handles both numerical and categorical data.
Good prediction accuracy.
Suitable for banking customer churn prediction.

Future Improvements
Hyperparameter tuning using GridSearchCV.
Cross-validation for better model evaluation.
Feature importance analysis.
Compare with Logistic Regression, Decision Tree, SVM, and XGBoost.
Deploy the model using Flask or Streamlit.
