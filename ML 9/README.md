# Task 8: Phishing Website Detection Using Machine Learning

## Project Overview
This project uses Machine Learning to identify phishing websites based on URL-related features. A Linear Support Vector Classification (Linear SVM) model is trained to classify websites into two categories: phishing and legitimate.

The project uses Python and Scikit-learn to preprocess the dataset, train the model, make predictions, and evaluate its performance.

---

## Objectives
- Analyze the phishing website dataset.
- Handle missing and infinite values.
- Prepare numerical features for machine learning.
- Train a Linear SVM classification model.
- Evaluate model performance using classification metrics.
- Visualize the confusion matrix and ROC curve.

---

## Technologies Used
- **Python** – Programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Data visualization library
- **Scikit-learn** – Machine learning and model evaluation
- **Jupyter Notebook** – Development environment

---

## Dataset
**Dataset:** PhiUSIIL Phishing URL Dataset

The dataset contains URL-related features used to train the classification model. The `label` column is used as the target variable, while columns such as `URL`, `Domain`, `TLD`, and `Title` are excluded from the input features.

---

## Project Workflow
1. **Load the dataset:** Read the CSV file using Pandas.
2. **Explore the data:** Check the dataset shape, columns, and missing values.
3. **Clean the data:** Remove rows with missing target labels and handle missing or infinite numerical values.
4. **Prepare features:** Select numerical columns and separate the target variable.
5. **Split the dataset:** Divide the data into 80% training data and 20% testing data.
6. **Scale the features:** Use `StandardScaler` to standardize the input features.
7. **Train the model:** Train a Linear SVM classifier using `LinearSVC`.
8. **Make predictions:** Predict labels for the test dataset.
9. **Evaluate performance:** Calculate precision, recall, F1-score, and ROC-AUC.
10. **Visualize results:** Display the confusion matrix and ROC curve.

---

## Machine Learning Algorithm
**Linear Support Vector Classification (LinearSVC)**

LinearSVC is a supervised machine learning algorithm used for classification. It learns a decision boundary that separates different classes based on the input features.

The model uses `class_weight="balanced"` to help address class imbalance in the training data.

---

## Evaluation Metrics
- **Precision:** Measures how many predicted positive cases are actually positive.
- **Recall:** Measures how many actual positive cases are correctly identified.
- **F1-score:** Combines precision and recall into a single metric.
- **ROC-AUC:** Measures the model's ability to distinguish between the two classes.
- **Confusion Matrix:** Shows correct and incorrect predictions for each class.
- **Classification Report:** Provides precision, recall, F1-score, and support for each class.

---

## How to Run the Project
1. Download or clone the project repository.
2. Download the dataset and place it in the appropriate location.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

4. Open `Task_8.ipynb` in Jupyter Notebook or Google Colab.
5. Update the dataset file path if necessary.
6. Run the notebook cells in order.
7. Review the evaluation metrics and visualizations.

---

## Author 

Madhumidha E
