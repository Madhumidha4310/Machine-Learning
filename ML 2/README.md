# Customer Segmentation using RFM Analysis and K-Means Clustering

## 📌 Project Overview

This project performs customer segmentation using RFM (Recency, Frequency, Monetary) analysis and K-Means clustering.

The sales transaction data is cleaned and prepared before calculating customer-level RFM metrics. The RFM values are then standardized and used with K-Means clustering to group customers based on their purchasing behavior.

The project also evaluates the clustering results using Silhouette Score and Davies-Bouldin Index and visualizes the resulting customer clusters.

---

## 🎯 Objectives

- Clean and preprocess sales transaction data.
- Remove invalid and cancelled transactions.
- Calculate the total transaction amount.
- Perform customer-level RFM analysis.
- Standardize RFM features.
- Segment customers using K-Means clustering.
- Determine a suitable number of clusters using the Elbow Method.
- Evaluate clustering performance.
- Visualize customer segments and summarize cluster characteristics.

---

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

## 📂 Dataset

The project uses a sales transaction dataset containing information such as:

- Customer ID
- Invoice
- Invoice Date
- Quantity
- Price

The dataset is loaded from a CSV file.

## 🔄 Project Workflow

```text
Sales Transaction Dataset
          ↓
Data Loading
          ↓
Data Exploration
          ↓
Data Cleaning
          ↓
Remove Cancelled Transactions
          ↓
Remove Invalid Transactions
          ↓
Remove Duplicates
          ↓
Calculate Total Amount
          ↓
RFM Analysis
          ↓
Feature Scaling
          ↓
Elbow Method
          ↓
K-Means Clustering
          ↓
Cluster Evaluation
          ↓
Customer Cluster Visualization
          ↓
Cluster Summary
```
---

## 🧹 Data Cleaning

The following preprocessing steps were performed:

1. Missing Customer IDs

Records without a Customer ID were removed.

2. Cancelled Invoices

Cancelled invoices were identified using the invoice information and removed from the dataset.

3. Invalid Transactions

Transactions with:

Quantity ≤ 0
Price ≤ 0

were removed.

4. Duplicate Records

Duplicate transaction records were removed.

### 💰 Total Amount Calculation

A new TotalAmount column was created:
```text
df["TotalAmount"] = df["Quantity"] * df["Price"]
```

This represents the total value of each transaction.

### 📊 RFM Analysis

RFM analysis was performed at the customer level.

Recency

Measures how recently a customer made a purchase.
```text
Recency = Reference Date - Last Purchase Date
```

A lower Recency value indicates that the customer purchased more recently.

Frequency

Measures how often a customer made purchases.

In this project, frequency is calculated using the number of unique invoices.

Monetary

Measures the total amount spent by the customer.

Monetary = Sum of TotalAmount

The three metrics are calculated using customer-level aggregation:

```text
rfm = df.groupby("Customer ID").agg(
    Recency=("InvoiceDate",
             lambda x: (reference_date - x.max()).days),
    Frequency=("Invoice", "nunique"),
    Monetary=("TotalAmount", "sum")
)
```
### ⚖️ Feature Scaling

The RFM features are standardized using StandardScaler:

```text
features = ["Recency", "Frequency", "Monetary"]

scaler = StandardScaler()

rfm_scaled = scaler.fit_transform(rfm[features])
```

Scaling ensures that features with different numerical ranges can be used effectively by the clustering algorithm.

### 🤖 K-Means Clustering

K-Means clustering is used to divide customers into groups based on their RFM characteristics.

The project initially evaluates different values of K using the Elbow Method.

```text
for k in range(2, 11):
    model = KMeans(
        n_clusters=k,
        random_state=42,
        n_init=10
    )

    model.fit(rfm_scaled)
    inertia.append(model.inertia_)
```

The final clustering model in the notebook uses:

n_clusters = 2

### 📉 Elbow Method

The Elbow Method is used to analyze the relationship between:

Number of clusters
Inertia

The resulting graph helps identify a suitable number of clusters for customer segmentation.

### 📏 Model Evaluation

Two clustering evaluation metrics are used.

Silhouette Score

The Silhouette Score measures how well customers are separated between clusters.

```text
silhouette = silhouette_score(
    rfm_scaled,
    rfm["Cluster"]
)
```
Davies-Bouldin Index

The Davies-Bouldin Index evaluates the similarity between clusters.

```text
db_index = davies_bouldin_score(
    rfm_scaled,
    rfm["Cluster"]
)
```

### 📈 Customer Cluster Visualization

Customer segments are visualized using:

Frequency on the X-axis
Monetary on the Y-axis
Cluster represented using different plot groups
```text
plt.scatter(
    rfm["Frequency"],
    rfm["Monetary"],
    c=rfm["Cluster"]
)
```
This helps visually understand differences in customer purchasing behavior.

### 📋 Cluster Summary

The average RFM values for each customer segment are calculated:

```text
cluster_summary = rfm.groupby("Cluster")[
    ["Recency", "Frequency", "Monetary"]
].mean()
```

This summary can be used to understand the characteristics of each customer group.

---

## 💡 Business Applications

Customer segmentation can help businesses:

- Identify recently active customers.
- Identify frequent customers.
- Identify high-value customers.
- Develop targeted marketing campaigns.
- Improve customer retention strategies.
- Identify different customer purchasing patterns.
- Personalize offers and promotions.

---

## 📁 Project Structure

```text
Customer-Segmentation/
│
├── Customer_Segmentation.ipynb
├── sales2.xlsx - Sheet1.csv
└── README.md
```
---
## 🚀 Future Enhancements

- Experiment with different numbers of clusters.
- Create meaningful customer segment names such as High-Value, Loyal, and At-Risk based on cluster characteristics.
- Add additional customer behavior features.
- Build an interactive Power BI dashboard.
- Compare K-Means with other clustering algorithms.
- Automate customer segmentation for new transaction data.

---

## 👩‍💻 Author

Madhumidha E

Skills demonstrated:
Python • Pandas • NumPy • Data Cleaning • RFM Analysis • K-Means Clustering • Scikit-learn • Data Visualization • Machine Learning
