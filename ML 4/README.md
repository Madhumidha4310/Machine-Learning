# Electric Vehicle Price Prediction using Linear Regression

## 📌 Project Overview

This project uses **Linear Regression** to predict the price of electric vehicles based on their driving range.

The dataset contains information about different electric vehicles in India, including brand, model, price, range, power, and battery capacity.

The project demonstrates a basic machine learning workflow including data loading, data cleaning, feature selection, model training, prediction, and model evaluation.

---

## 🎯 Objectives

- Load and explore an electric vehicle dataset.
- Understand the structure and dimensions of the dataset.
- Handle missing values in important columns.
- Analyze the relationship between EV range and price.
- Build a Linear Regression model.
- Predict EV prices using vehicle range.
- Compare actual and predicted prices.
- Evaluate the model using MAE, MSE, RMSE, and R² Score.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab / Jupyter Notebook

---

## 📂 Dataset

The dataset contains **26 electric vehicle records** and **6 columns**.

### Dataset Columns

| Column | Description |
|---|---|
| Brand | EV manufacturer/brand |
| Model | Electric vehicle model |
| Price | Price of the vehicle |
| Range | Driving range of the EV |
| Power | Vehicle power |
| Battery | Battery capacity |

Example records include brands such as Maruti, Tata, Mahindra, and MG.

---

## 🔄 Project Workflow

```text
EV Dataset
    ↓
Data Loading
    ↓
Data Exploration
    ↓
Data Cleaning
    ↓
Missing Value Handling
    ↓
Feature Selection
    ↓
Train-Test Split
    ↓
Linear Regression
    ↓
Price Prediction
    ↓
Actual vs Predicted Visualization
    ↓
Model Evaluation
```
---

## 💡 Key Insights

- The project demonstrates the complete basic machine learning workflow.
- EV range has a positive relationship with predicted price in the trained Linear Regression model.
- Range alone is not sufficient to accurately predict EV prices in this dataset.
- The model can potentially be improved by including additional features such as Power and Battery capacity.
- The small dataset size also limits the reliability and generalization of the model.

---

## 🚀 Future Enhancements

- Include Power and Battery as additional features.
- Perform exploratory data analysis using visualizations.
- Compare Linear Regression with other regression algorithms.
- Perform feature scaling where appropriate.
- Use a larger EV dataset for better generalization.
- Perform cross-validation.
- Tune and compare different machine learning models.
- Build an interactive dashboard for EV price analysis.

---

## 📁 Project Structure

```text
Electric-Vehicle-Price-Prediction/
│
├── ML Task 4.ipynb
├── ev_car_India_dataset.csv
└── README.md

```

---

## 👩‍💻 Author

Madhumidha E
