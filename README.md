# Credit Card Fraud Detection

## 📌 Project Overview

This project uses **Machine Learning** to identify fraudulent credit card transactions.

The project implements a binary classification workflow using **Logistic Regression**, with exploratory data analysis, feature scaling, stratified train-test splitting, and model evaluation.

## 🎯 Objective

Identify **fraudulent credit card transactions** and distinguish them from legitimate transactions using the transaction features provided in the dataset.

## 📊 Dataset Overview

The dataset contains **284,807 transactions** and **31 columns**.

The features include:

- `Time`
- `Amount`
- Anonymized features `V1` to `V28`
- `Class` — target variable

### Target Variable

| Class | Meaning |
|---|---|
| `0` | Non-fraudulent transaction |
| `1` | Fraudulent transaction |

The dataset contains:

- **284,315** non-fraudulent transactions
- **492** fraudulent transactions

This demonstrates a strong **class imbalance**, which is an important consideration in fraud detection.

## 🛠️ Technologies & Libraries

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn
- Jupyter Notebook

### Machine Learning Techniques

- Train-Test Split
- Stratified Sampling
- StandardScaler
- Logistic Regression
- Confusion Matrix
- Classification Report
- Accuracy Score

## 🔄 Project Workflow

```text
Dataset
   ↓
Load & Explore Data
   ↓
Exploratory Data Analysis
   ↓
Handle Class Imbalance
   ↓
Feature Scaling
   ↓
Train-Test Split
   ↓
Logistic Regression
   ↓
Predictions
   ↓
Model Evaluation
```

## 🔍 Exploratory Data Analysis

The notebook includes analysis of:

- Fraud vs. non-fraud transaction counts
- Feature relationships
- Correlation between variables
- Transaction amount
- Transaction time
- Anonymized transaction features

A correlation heatmap is used to visualize relationships among the dataset features.

## 🧹 Data Preprocessing

The project performs preprocessing before model training.

### Feature Scaling

`StandardScaler` is used for the `Time` and `Amount` features.

The original columns are then removed and the processed features are arranged for model training.

## 🤖 Model Training

The project uses **Logistic Regression** for binary classification.

### Train-Test Split

The dataset is divided into training and testing sets using **stratification** so that the class distribution is preserved between the splits.

### Model

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
```

The trained model is then used to predict whether transactions are fraudulent or non-fraudulent.

## 📈 Model Evaluation

The model is evaluated using:

- **Accuracy Score**
- **Confusion Matrix**
- **Classification Report**

These evaluation methods help measure the model's classification performance and provide class-level metrics.

## ⚠️ Class Imbalance

Fraudulent transactions represent only a small portion of the complete dataset.

Because fraud detection is highly imbalanced, accuracy alone may not fully describe model performance. Precision, recall, F1-score, and the confusion matrix are also important when evaluating the model.

## 📁 Project Structure

```text
Credit-Card-Detection/
│
├── Credit_Card_Fraud_Detection_Structured_test.ipynb
├── creditcard.csv
└── README.md
```

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/bhaktibhanushali-01/Credit-Card-Detection.git
```

### 2. Navigate to the project

```bash
cd Credit-Card-Detection
```

### 3. Install dependencies

```bash
pip install pandas numpy seaborn matplotlib scikit-learn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Credit_Card_Fraud_Detection_Structured_test.ipynb
```

Make sure `creditcard.csv` is in the same project directory as the notebook.

## 🚀 Future Improvements

The notebook suggests exploring additional techniques to improve fraud detection, including:

- Random Forest
- XGBoost
- SMOTE for handling class imbalance
- Additional ensemble methods

## 💡 Key Takeaway

This project demonstrates an end-to-end **Credit Card Fraud Detection** workflow using Python and Machine Learning, covering data exploration, preprocessing, feature scaling, class-imbalance considerations, Logistic Regression, and model evaluation.

## 👩‍💻 Author

**Bhakti Bhanushali**
