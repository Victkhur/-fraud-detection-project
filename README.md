# Fraud Detection using Anomaly Detection & XGBoost

## 📌 Project Overview
Fraud detection is a critical challenge in the financial industry due to the high imbalance between fraudulent and legitimate transactions. This project explores **Anomaly Detection** techniques, including **Isolation Forest, Autoencoders, and XGBoost with SMOTE**, to identify fraudulent transactions effectively.

## 📂 Dataset
The dataset includes information about transactions made by credit cards in September 2013 by European cardholders. I will use the trained model to assess if a credit card transaction is legitimate or not. The dataset contains **284,807** transactions with the following distribution:
- **Legitimate Transactions (Class 0):** 99.83%
- **Fraudulent Transactions (Class 1):** 0.17%

Since fraud cases are extremely rare, **handling imbalanced data** is a key part of this project.

## 🔍 Approach & Models Used
### 1️⃣ **Isolation Forest (Unsupervised Learning)**
- Detects fraud based on how quickly an instance is isolated in decision trees.

### 2️⃣ **Autoencoder (Deep Learning)**
- A neural network trained to reconstruct normal transactions.
- High reconstruction error indicates possible fraud.

### 3️⃣ **XGBoost with SMOTE (Supervised Learning)**
- **XGBoost**: A gradient boosting algorithm.
- **SMOTE**: Synthetic Minority Over-sampling Technique to balance the dataset.

## ⚖ Handling Imbalanced Data
Since fraud cases are highly imbalanced, the following techniques were used:
-  **SMOTE** for oversampling fraudulent cases for XGBoost.
-  **Anomaly detection models** (Isolation Forest & Autoencoder), which do not require balanced data.

## 📊 Model Evaluation
Since accuracy alone is misleading for imbalanced data, we evaluated models using:
- **Precision-Recall (PR) Curve**
- **AUC-ROC Score**
- **F1-Score**

### **Precision-Recall Curve Results:**
- **Isolation Forest AUC = 0.135**
- **Autoencoder AUC = 0.170**
- **XGBoost AUC = 0.990** ✅

📊 **XGBoost outperformed anomaly detection models**, making it the best choice for fraud detection!

## 🔍 Feature Importance using SHAP
To understand which features contribute most to fraud detection, we used **SHAP values**. The top fraud indicators were:
- **V12, V14, and V17** (strong indicators of fraudulent behavior)
- **Transaction Amount** (some fraudulent transactions had unusual amounts)

## 🚀 Installation & Running the Project
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/YOUR_USERNAME/fraud-detection-project.git
cd fraud-detection-project
```

### **2️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

### **3️⃣ Run the Jupyter Notebook**
```bash
jupyter notebook
```
Open the notebook and run all cells to execute the project.

## 📂 Project Structure
```
fraud-detection-project/
│── notebooks/           # Jupyter notebooks
│── requirements.txt     # List of dependencies
│── README.md            # Project overview
```

## 📂 Dataset
If the dataset is too large, download it manually from Kaggle:  
🔗 **[Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)**

## 📢 Contributing
Feel free to contribute by submitting a pull request! 😊

## 📬 Contact
If you have any questions, reach out to me on **LinkedIn** or **GitHub**!

---
🚀 **Star this repository** if you find it useful! ⭐

