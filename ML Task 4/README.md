# Customer Feedback Classification Using Machine Learning

## Project Overview

This project focuses on automatically classifying customer feedback into different categories using Machine Learning and Natural Language Processing (NLP).

The system analyzes customer feedback messages and predicts the appropriate category based on the text content. This can help businesses organize customer queries and route them to the correct department.

---

## Categories

The customer feedback is classified into the following categories:

- Billing
- General Inquiry
- Technical Support
- Delivery
- Product

---

## Dataset

The dataset contains two main columns:

- Feedback – The customer's message or complaint.
- Category – The corresponding category of the customer feedback.

The dataset includes customer feedback related to billing issues, product problems, delivery concerns, technical difficulties, and general questions.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Natural Language Processing (NLP)
- TF-IDF Vectorization
- Machine Learning Classification

---

## Project Workflow

- 1.Load the customer feedback dataset. 
- 2.Explore and understand the dataset. 
- 3.Check the distribution of feedback categories.
- 4.Preprocess the text data.
- 5.Convert text into numerical features using TF-IDF Vectorization.
- 6.Split the dataset into training and testing data.
- 7.Train a Machine Learning classification model.
- 8.Predict categories for unseen customer feedback.
- 9.Evaluate model performance using accuracy and classification metrics.
- 10.Test the model with new customer feedback.

---

## Model Evaluation

The model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report

These evaluation metrics help determine how effectively the model classifies customer feedback into the correct categories.

---

## Sample Categories

### Product

Examples of product-related feedback include:

- Wrong color received and I need help.
- Wrong size received.
- Product arrived broken.
- Button not working.
- Device overheats.

### General Inquiry

Examples include:

- Is gift wrapping available?
- Can I change my address?
- Can I cancel my order?
- Do you offer discounts?

### Technical Support

Examples include:

- Checkout page not loading.
- Password reset not working.
- Cannot log in.
- Search feature not working.
- Mobile app closes automatically.

### Delivery

Examples include:

- Package not received.
- Order still in transit.
- Package not received since yesterday.
- Courier delivered to the wrong address.

### Billing

Examples include:

- Refund is delayed.
- Invoice is incorrect.
- I was charged twice.
- Refund not received.

---

## Project Structure

Customer-Feedback-Classification/
│
├── README.md
├── Customer_feedback.xlsx
├── customer_feedback_classification.ipynb
│
└── Output/
    ├── classification_report.txt
    └── model_results.txt
    
## How to Run the Project

Step 1: Install Required Libraries
pip install pandas openpyxl scikit-learn numpy

Step 2: Open the Notebook
Open the following file using Google Colab or Jupyter Notebook:
customer_feedback_classification.ipynb

Step 3: Upload Dataset
Upload:
Customer_feedback.xlsx

Step 4: Run the Notebook
Execute all cells in order.

Step 5: Check Results
The notebook will display:

- Dataset information
- Category distribution
- Model predictions
- Accuracy
- Classification report
- Predictions for new customer feedback

---

## Applications

This project can be used in:

- Customer Support Automation
- Help Desk Systems
- E-commerce Platforms
- Complaint Management Systems
- Automated Ticket Classification
- Customer Service Chatbots

---

## Future Enhancements

- Add more customer feedback data.
- Improve text preprocessing.
- Compare multiple Machine Learning algorithms.
- Use Deep Learning models for better text classification.
- Create a web-based interface for real-time predictions.
- Integrate the model with a customer support system.
- Deploy the trained model as an online API.
