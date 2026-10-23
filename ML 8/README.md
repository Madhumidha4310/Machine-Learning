# Credit Card Fraud Detection Using Machine Learning

## Project Overview
This project detects fraudulent credit card transactions using Machine Learning. It uses the Random Forest Classifier to classify transactions as genuine or fraudulent.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## Algorithm
**Random Forest Classifier**

## Dataset
- File name: `creditcard.csv`
- Target column: `Class`
- `0` – Genuine transaction
- `1` – Fraudulent transaction

## Project Workflow
1. Load the credit card dataset.
2. Explore and analyze the data.
3. Check missing values.
4. Separate features and target values.
5. Split the data into training and testing sets.
6. Train the Random Forest model.
7. Predict fraudulent transactions.
8. Evaluate model performance.
9. Display confusion matrix and ROC curve.
10. Identify important features.
11. Export actual fraudulent test transactions to a CSV file.

## Evaluation Metrics
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report

## Installation

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## How to Run
1. Download or obtain the `creditcard.csv` dataset.
2. Open the Python notebook in Google Colab or Jupyter Notebook.
3. Update the dataset path if necessary.
4. Run all cells.
5. View the model evaluation results and graphs.

## Output
- Predicted transaction labels
- Fraud probability
- Confusion matrix
- Classification report
- Feature importance graph
- ROC curve
- CSV file containing actual fraudulent test transactions

## Note
This project is intended for educational purposes. Model performance should be evaluated carefully before considering real-world fraud detection use.

## Author

Madhumidha 
