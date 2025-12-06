# 💳 Credit Card Customer Segmentation & Classification

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Active-orange?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)

**A dual-stage Machine Learning project that first identifies distinct customer profiles using Unsupervised Clustering (K-Means) and then builds a Supervised Classification model to predict segments for new customers with 94% accuracy.**

## 🎯 Objectives
The primary goals of this project are:
1.  **Analyze Customer Behavior:** Explore credit card usage patterns to understand different spending and payment behaviors.
2.  **Market Segmentation:** Group customers into distinct clusters using Unsupervised Learning to aid in targeted marketing strategies.
3.  **Predictive Modeling:** Build a robust classification model that can instantly assign a new customer to one of the identified segments based on their financial data.

## 📊 Dataset Overview
The dataset contains usage statistics for **8,950 active credit card holders** over the last 6 months.

| Feature | Description |
| :--- | :--- |
| **BALANCE** | Balance amount left in the account to make purchases |
| **PURCHASES** | Amount of purchases made from the account |
| **CASH_ADVANCE** | Cash in advance given by the user |
| **CREDIT_LIMIT** | Limit of Credit Card for user |
| **PAYMENTS** | Amount of Payment done by user |
| **MINIMUM_PAYMENTS** | Minimum amount of payments made by user |
| **TENURE** | Tenure of credit card service for user |
| **PRC_FULL_PAYMENT** | Percent of full payment paid by user |

## 🏆 Model Performance

The project employs a two-step approach. First, **K-Means Clustering** defines the targets, and then a **Decision Tree Classifier** learns to predict them.

| Approach | Algorithm | Key Metric | Result |
| :--- | :--- | :--- | :--- |
| **Unsupervised** | K-Means Clustering | Silhouette Score | Optimal Clusters: **4** |
| **Supervised** | Decision Tree Classifier | **Accuracy** | **94%** |

## 🚀 Key Features Implemented

✅ **Data Preprocessing:** Handling missing values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT`  
✅ **Dimensionality Reduction:** Applied **PCA (Principal Component Analysis)** to reduce noise and improve clustering performance  
✅ **Optimal K Selection:** Used the **Elbow Method** and **Silhouette Analysis** to determine the ideal number of segments (4)  
✅ **Clustering:** Implemented **K-Means**, **Agglomerative**, and **Spectral Clustering** (K-Means selected as final)  
✅ **Supervised Learning:** Trained a **Decision Tree Classifier** to predict customer segments  
✅ **Model Persistence:** Saved the final classification model using `pickle` for future use  


## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-learn (PCA, K-Means, DecisionTree, StandardScaler)
* **Utilities:** Pickle (Model Saving)

## 🎯 Quick Start

### 1. Clone the Repository

[git clone](https://github.com/obasama697/Market_Segmentation_Python_Model/tree/main)


### 2. Install Dependencies
```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

### 3. Run the Notebook
Open Market_segment_customer_data.ipynb in Jupyter Notebook or Google Colab and execute the cells to reproduce the analysis.

### 4. Use the Saved Model
```bash

import pickle

# Load the trained Decision Tree model
filename = 'final_model.sav'
loaded_model = pickle.load(open(filename, 'rb'))

# Predict segment for a new customer (example data)
# result = loaded_model.predict(new_customer_data)
```

## 📈 Key Insights (The 4 Segments)
Based on the clustering analysis, customers were grouped into 4 distinct personalities:

* Cluster 0: Customers with low balance and low spending (Inactive/Low-value).
* Cluster 1: Customers with high balance but low purchase frequency (Potential churners/Savers).
* Cluster 2: High purchase frequency and high payments (Gold/Loyal customers).
* Cluster 3: High cash advance usage (High-risk/Credit seekers).

## 📁 Project Structure
```bash

├── Market_segment_customer_data.ipynb  # 📓 Main analysis notebook
├── Customer Data.csv                   # 💾 Dataset
├── Clustered Customer Data.csv         # 💾 Dataset
├── final_model.sav                     # 🤖 Trained Decision Tree model
├── README.md                           # 📄 Documentation
```

## 🤝 Contributing
Contributions are welcome!
Fork the project.
Create your feature branch (git checkout -b feature/NewAlgorithm).
Commit your changes.
Push to the branch and open a Pull Request.

Built with 💻 and ☕ by [[Rupal](https://github.com/obasama697)] | 94% Classification Accuracy

## Stay Updated and connected
- **LinkedIn**: [Connect with me professionally](https://www.linkedin.com/in/rupal--tripathi/)


Thank you for your support, and I look forward to connecting with you!
