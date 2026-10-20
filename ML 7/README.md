# Decision Tree-Based Phishing URL Detection

## Project Overview
This project uses a Decision Tree Classifier to classify URL records as legitimate or phishing based on numeric features in the PhiUSIILPhishing URL Dataset. 
It uses Python and common data science libraries to prepare the data, train the model, visualize the decision tree, and evaluate its performance.

---

## Objectives

- Load and inspect the phishing URL dataset.
- Prepare numeric features and handle missing or infinite values.
- Split the dataset into training and testing sets.
- Train a Decision Tree classification model.
- Visualize the decision tree and confusion matrix.
- Evaluate the model using accuracy, precision, recall, F1-score, and
  specificity.

---

## Technologies and Libraries
- Python
- NumPy
- pandas
- Matplotlib
- Seaborn
- scikit-learn

---

## Dataset

The notebook expects a CSV file named:

```
PhiUSIIL_Phishing_URL_Dataset - PhiUSIIL_Phishing_URL_Dataset.csv
```

The original code uses a Google Colab path:

```
/content/PhiUSIIL_Phishing_URL_Dataset - PhiUSIIL_Phishing_URL_Dataset.csv
```

Update this path if the dataset is stored in a different location. The
dataset must include a column named label and numeric feature columns.

---

## Installation

Install the required libraries:
```
pip install numpy pandas matplotlib seaborn scikit-learn
```

How to Run
1. Download the dataset and place it in the location used by the code,
   or update the CSV path.
2. Open Decision_Tree.ipynb in Google Colab or Jupyter Notebook. If
   using the supplied Python script, run it in an environment where the
   dataset path is accessible.
3. Execute the code cells in order.
4. Review the decision-tree visualization, confusion matrix, and
   evaluation metrics.
Project Workflow
1. Import libraries: Load tools for data processing, visualization,
   model training, and evaluation.
2. Explore the dataset: Display sample rows, data types, summary
   statistics, dataset shape, column names, missing values, and label
   counts.
3. Prepare the target: Remove rows with missing target labels and
   transform the label column into a binary target.
4. Prepare features: Select numeric columns other than label,
   replace infinite values with missing values, and fill missing
   feature values using each column's median.
5. Split the data: Use an 80% training set and a 20% testing set,
   with stratification to preserve class proportions.
6. Train the model: Fit a DecisionTreeClassifier with
   max_depth=5, class_weight="balanced", and random_state=42.
7. Visualize the tree: Plot the trained decision tree with feature
   names and class labels.
8. Predict and evaluate: Generate test predictions, display a
   confusion matrix, and calculate evaluation metrics.

---

## Evaluation Metrics

- Accuracy: Proportion of all predictions that are correct.
- Precision: Proportion of predicted positive cases that are
  actually positive.
- Recall: Proportion of actual positive cases correctly
  identified.
- F1-score: Harmonic mean of precision and recall.
- Specificity: Proportion of actual negative cases correctly
  identified.
- Confusion matrix: Shows counts of correct and incorrect
  predictions for each class.

The program prints the metric values when it runs. Actual results depend
on the dataset and the environment, so no fixed scores are stated here.

---

## Important Label-Mapping Note

The code creates the target with:
```
y = (df["label"] == 0).astype(int)
```
This means rows whose original label is 0 become target class 1, while all other non-missing labels become target class 0. Before interpreting the displayed class names (Legitimate and Phishing), verify what 0 and the other values mean in the source dataset. If the mapping does not match the class names, update either the target transformation or the displayed class names.

---

## Limitations and Improvements

- The dataset CSV must be available at the configured path.
- The code uses numeric features only; non-numeric columns are
  excluded.
- The decision tree is limited to a depth of five, which may affect
  model performance.
- Confirm the dataset's label meanings before using the model's
  predictions.
- For a more robust evaluation, consider cross-validation, parameter
  tuning, and testing on an independent dataset.

---

## Project Structure

```
project/
├── decision_tree.py
├── Decision_Tree.ipynb
├── PhiUSIIL_Phishing_URL_Dataset - PhiUSIIL_Phishing_URL_Dataset.csv
└── README.md
```

---

## 👩‍💻 Author

Madhumidha E
