# Amazon E-Commerce Sales Analysis & Price Prediction using Machine Learning

## Project Overview

This project focuses on analyzing Amazon e-commerce data and building a Machine Learning model to predict product prices using Linear Regression.

The project uses a large-scale Amazon e-commerce dataset containing product details, customer information, sales information, ratings, discounts, and transaction details. Data preprocessing, exploratory data analysis, visualization, and predictive modeling are performed using Python.

---

## Objectives

- Analyze Amazon e-commerce sales trends.
- Clean and preprocess large-scale e-commerce data.
- Handle missing values and categorical data.
- Perform sales trend analysis.
- Identify top-performing brands.
- Build a Machine Learning model to predict product prices.
- Evaluate model performance using regression metrics.

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

## Machine Learning Algorithm

### Linear Regression

Linear Regression is used to predict the final product price based on various product and customer-related features.

### Features Used

- Category
- Subcategory
- Brand
- Product Price
- Discount
- Rating
- Review Count
- Stock Availability
- Seller Rating
- Shipping Time
- Location
- Device Type
- Payment Method
- Delivery Status
- Return Status
- Purchase Date Information

### Target Variable

- Final Price

---

## Project Workflow

### 1. Data Collection

The Amazon e-commerce dataset is loaded using Pandas.

Dataset contains:

- Product details
- Customer details
- Sales information
- Ratings and reviews
- Transaction information

---

### 2. Data Preprocessing

Performed data cleaning operations:

- Checking dataset structure
- Handling missing values
- Filling numerical missing values using mean
- Filling categorical missing values using mode
- Converting date columns into datetime format
- Encoding categorical variables using Label Encoder

---

### 3. Exploratory Data Analysis

Performed analysis using visualizations:

- Monthly sales trend analysis
- Top 10 brands based on sales
- Product price distribution analysis

Visualization libraries used:

- Matplotlib

---

### 4. Feature Selection

Selected important features for training the Machine Learning model.

Category
Brand
Price
Discount
Rating
Review Count
Stock
Seller Rating
Shipping Time
Location
Device
Payment Method
Return Status
Delivery Status
Date Features


---

### 5. Model Training

Dataset is divided into:

- Training Data: 80%
- Testing Data: 20%

Machine Learning Model:


---

### 6. Model Evaluation

The model performance is evaluated using:

### R2 Score

Measures how well the model explains the variation in price prediction.

### MAE (Mean Absolute Error)

Measures average prediction error.

### MSE (Mean Squared Error)

Measures squared prediction errors.

### RMSE (Root Mean Squared Error)

Measures prediction accuracy.

---

## Results

The model predicts product prices based on different e-commerce attributes.

The evaluation metrics generated:

- R2 Score
- MAE
- MSE
- RMSE
- Model Accuracy Percentage

The project also generates:

- Monthly sales trend visualization
- Actual vs Predicted price comparison graph
- Top brands sales analysis

---

## Project Structure

Amazon-Price-Prediction/
│
├── Amazon_Ecommerce_Analysis.ipynb
│
├── README.md
│
└── Dataset/
└── amazon_ecommerce_1M.csv


---

## How to Run the Project

Step 1: Clone Repository
[ML Task 2](https://github.com/Madhumidha4310/Machine-Learning/tree/639594b867a8e52eab02d4140fbd3d385c604e0d/ML%20Task%202)

Step 2: Install Required Libraries
pip install pandas numpy matplotlib scikit-learn

Step 3: Open Jupyter Notebook

jupyter notebook

Step 4:
Open the notebook file and run all cells.

## Future Improvements

Implement advanced ML algorithms like Random Forest and XGBoost.
Create an interactive dashboard using Power BI or Streamlit.
Perform customer segmentation.
Build a real-time price prediction application.
Improve prediction accuracy using hyperparameter tuning.

## Author

Madhumidha E

Bachelor of Computer Applications (BCA)

Kamaraj College
