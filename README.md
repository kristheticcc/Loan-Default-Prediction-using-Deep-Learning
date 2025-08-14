# 🏦🤖 Loan Default Prediction using Deep Learning

This project builds and trains a **Deep Neural Network (DNN)** to predict whether a borrower will **fully repay** their loan or **default (Charged Off)** using financial and personal data from LendingClub. The project includes extensive **Exploratory Data Analysis (EDA)**, **data cleaning & feature engineering**, and a **TensorFlow/Keras-based deep learning model** for binary classification.

---

## 📑 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [How to Use](#how-to-use)
- [Model Performance](#model-performance)
- [Author](#author)

---

## 📌 Project Overview

The goal of this project is to build a predictive model that can determine the likelihood of a loan being **fully paid** or **charged off**, based on a variety of borrower and loan features.  
This model can assist financial institutions in **risk assessment** and **decision-making** during the loan approval process.

---

## 📊 Dataset

- **Files Used:**
  - `lending_club_loan_two.csv` (loan records including status and borrower details)
  - `lending_club_info.csv` (feature descriptions)

- **Source:** 
  - [lending_club_loan_two.csv](https://www.kaggle.com/datasets/epsilon22/lending-club-loan-two) 
  - [lending_club_info.csv](https://www.kaggle.com/datasets/gabrielsantello/lending-club-loan-preprocessed-dataset/data)

---

## 🔍 Key Features

### 1. 🧪 Exploratory Data Analysis (EDA)
- Countplot of loan status (Fully Paid vs Charged Off)
- Histogram of loan amount distributions
- Boxplots grouped by repayment status
- Grade and Sub-grade comparisons
- Correlation heatmap of numeric features
- Scatterplot between loan amount and installment

### 2. 🧹 Data Preprocessing
- Created binary target column `loan_repaid` (1 = Fully Paid, 0 = Charged Off)
- Handled missing values using grouped mean imputation
- Dropped high-cardinality and redundant columns (e.g., `emp_title`, `title`, `issue_d`)
- Converted date columns and extracted year features
- Created dummy variables for categorical features (e.g., `home_ownership`, `purpose`, `sub_grade`)
- Normalized features using `MinMaxScaler`

### 3. 🧠 Deep Learning Model
- Implemented using **TensorFlow/Keras**
- Architecture:
  - Input layer: All numeric & one-hot encoded features
  - 3 Hidden layers with ReLU activation and Dropout
  - Output layer with sigmoid activation (binary classification)
- Compiled with:
  - Loss: `binary_crossentropy`
  - Optimizer: `adam`
- Trained for **25 epochs** with **batch size = 250**

### 4. 📈 Evaluation
- Visualized training vs validation loss
- Used `confusion_matrix` and `classification_report` from `sklearn`
- Made real-world predictions on randomly selected borrower data

---
## 🛠️ How to Use?

1. **Clone the repository**
2. **Download the dataset from Kaggle from the provided link**
3. **Install required libraries**
- Python 3+
- Required libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - tensorflow (has to be compatable with Keras)
   
Run the Jupyter Notebook
Open the notebook in Jupyter Notebook
Execute cells step-by-step

👨‍💻 Author

Krish Makwana
