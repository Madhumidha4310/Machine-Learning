# 🏠 Real Estate Price Analysis and Property Clustering using Machine Learning

## 📌 Project Overview

This project focuses on analyzing real estate property data and grouping properties based on location, price, and area using Machine Learning techniques.

The project uses **K-Means Clustering Algorithm** to identify different property groups and creates an interactive map using **Folium** to visualize property locations with different price categories.

---

## 🎯 Objectives

- Analyze real estate property datasets
- Clean and preprocess property data
- Apply Machine Learning clustering techniques
- Identify property groups based on price, location, and area
- Classify properties into different levels:
  - Classic
  - Affordable
  - Luxury
- Visualize properties using an interactive map

---

## 📂 Dataset Description

The project uses two datasets:

- `train_part1.csv`
- `train_part2.csv`

Both datasets are merged into a single dataset for analysis.

### Important Features:

| Feature | Description |
|---------|-------------|
| Latitude | Property latitude location |
| Longitude | Property longitude location |
| Locality | Area/location name |
| Price_INR | Property price in Indian Rupees |
| SuperBuiltUpArea_sqft | Property area in square feet |

---

## 🛠️ Technologies Used

### Programming Language
- Python

### Libraries

- Pandas → Data processing
- NumPy → Numerical operations
- Matplotlib → Data visualization
- Folium → Interactive map visualization
- Scikit-learn → Machine Learning algorithms

---

## 🔄 Project Workflow

### 1. Import Required Libraries

Libraries required for data analysis, visualization, and clustering are imported.

---

### 2. Data Loading

Two real estate datasets are loaded:
train_part1.csv
train_part2.csv

The datasets are combined into one dataframe.

---

### 3. Data Cleaning

Performed preprocessing operations:

- Checking missing values
- Removing duplicate records
- Selecting required columns
- Handling missing data
- Converting columns into numeric format

Final cleaned dataset:

Cleaned_Dataset.csv

---

## 📊 Exploratory Data Analysis

The project analyzes:

- Property price distribution
- Property area
- Location information

A statistical summary is generated to understand the dataset.

---

# 🤖 Machine Learning Model

## K-Means Clustering

K-Means clustering is used to group similar properties.

### Selected Features:

Latitude
Longitude
Price_INR
SuperBuiltUpArea_sqft


---

## Feature Scaling

StandardScaler is applied to normalize numerical values before clustering.

---

## Finding Optimal Clusters

The Elbow Method is used to identify the suitable number of clusters.

Output:

<img width="800" height="500" alt="Elbow_Method" src="https://github.com/user-attachments/assets/9caa9e99-9612-4288-9d45-e223521597cb" />

---

## Model Training

K-Means algorithm is applied with:


Each property is assigned to a cluster.

Output:

Clustered_House_Data.csv


---

# 📈 Visualization

## Area vs Price Visualization

A scatter plot is created to understand the relationship between property area and price.

Output:

<img width="1000" height="600" alt="Area_vs_Price" src="https://github.com/user-attachments/assets/8208708c-4312-4c72-8616-fd363947a708" />

---

# 🏷️ Property Classification

Properties are categorized based on price:

### Classic
Lower price range properties

### Affordable
Medium price range properties

### Luxury
High price range properties

---

# 🗺️ Interactive Real Estate Map

Folium is used to create an interactive map.

Features:

- Property location markers
- Marker clustering
- Popup information

Each property displays:

Location
Price
Area
Property Level


Marker Colors:

| Property Type | Marker Color |
|--------------|--------------|
| Luxury | Red |
| Affordable | Blue |
| Classic | Green |

---

# 📁 Project Outputs

| File Name | Description |
|-----------|-------------|
| Cleaned_Dataset.csv | Cleaned property dataset |
| Clustered_House_Data.csv | Dataset with cluster labels |
| Elbow_Method.png | Cluster selection graph |
| Area_vs_Price.png | Price and area visualization |
| Real_Estate_Map.html | Interactive property map |

---

# 🚀 How to Run the Project

## Step 1: Install Required Libraries

- `pip install pandas numpy matplotlib folium scikit-learn`

Step 2: Upload Dataset

Place these files:

- `train_part1.csv`
- `train_part2.csv`

Step 3: Run Notebook

Open:

- `Real_Estate_Clustering.ipynb`

Run all cells.

📌 Future Improvements
Add Deep Learning based price prediction
Build a web dashboard
Add real-time property data
Implement house price prediction model
Deploy using Streamlit
👩‍💻 Author

Madhumidha E

BCA Student
