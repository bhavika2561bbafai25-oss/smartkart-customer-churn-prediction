# smartkart-customer-churn-prediction
“An end-to-end Machine Learning project using Logistic Regression to predict customer churn, with data cleaning, preprocessing, model evaluation, and business-ready risk reporting.”
# 🛒 SmartKart — Customer Churn Prediction

An end-to-end Machine Learning project that predicts whether SmartKart customers are likely to churn using **Logistic Regression**.

The project demonstrates a complete ML pipeline, starting from a messy customer dataset and ending with a business-ready customer churn risk report.

---

## 📌 Project Overview

SmartKart is an e-commerce business that wants to identify customers who are likely to leave the platform.

The objective of this project is to use customer information such as:

* Age
* Monthly Spending
* Number of Complaints

to predict whether a customer is likely to **Churn** or **Not Churn**.

The project uses a deliberately messy dataset containing duplicates, missing values, invalid entries, and outliers to demonstrate real-world data preprocessing.

---

## 🎯 Objectives

* Understand a real-world Machine Learning pipeline.
* Clean and preprocess messy customer data.
* Detect and treat outliers.
* Select meaningful features.
* Define and prepare the target variable.
* Split data into training and testing sets.
* Standardise numerical features.
* Build a Logistic Regression model.
* Make customer churn predictions.
* Evaluate model performance.
* Interpret model coefficients.
* Generate a business-ready churn risk report.

---

## 📊 Dataset

**Dataset:** `SmartKart_dirty_100_rows.csv`

The original dataset contains **100 customer records** with the following columns:

| Column        | Description                   |
| ------------- | ----------------------------- |
| Customer_ID   | Unique customer identifier    |
| Age           | Customer age                  |
| Monthly_Spend | Customer's monthly spending   |
| Complaints    | Number of customer complaints |
| Churn         | Target variable               |

### Target Variable

* `0` = No Churn
* `1` = Churn

The dataset intentionally contains data-quality problems such as duplicates, missing values, incorrect data types, invalid values, and extreme outliers.

---

## 🔄 Machine Learning Pipeline

The project follows a complete **15-step ML pipeline**:

1. Data Collection
2. Data Understanding
3. Data Cleaning
4. Outlier Detection & Treatment
5. Feature Selection
6. Define Target Variable
7. Encode Target Variable
8. Train-Test Split
9. Feature Standardisation
10. Model Building
11. Model Training
12. Prediction
13. Model Evaluation
14. Model Interpretation
15. Final Business Output

---

## 🧹 Data Cleaning

The dataset is cleaned by:

* Removing duplicate records
* Removing unnecessary whitespace
* Converting text values into numeric values
* Correcting invalid age values
* Handling negative spending values
* Filling missing values using the median

After cleaning, the dataset contains **95 customer records** and no remaining missing values.

---

## 📈 Outlier Treatment

The project uses the **IQR (Interquartile Range) method** to identify extreme values.

Outliers are capped instead of removing entire customer records.

Examples include:

* Extremely high monthly spending
* Unrealistically high complaint counts

This helps prevent extreme values from disproportionately affecting the Logistic Regression model.

---

## 🔍 Feature Selection

The following features are used for prediction:

```text
Age
Monthly_Spend
Complaints
```

`Customer_ID` is excluded because it is an identifier rather than a meaningful predictive feature.

---

## 🤖 Machine Learning Model

### Logistic Regression

Logistic Regression is used because customer churn is a **binary classification problem**.

The model predicts:

```text
0 → No Churn
1 → Churn
```

It also produces a **churn probability**, which can be useful for identifying customers who may require retention attention.

---

## ⚙️ Feature Standardisation

The numerical features are standardised using:

**StandardScaler**

The scaler is fitted only on the training data and then applied to the test data.

This prevents information from the test set from leaking into the training process.

---

## 🧪 Model Evaluation

The model is evaluated using:

* Confusion Matrix
* Accuracy
* Precision
* Recall
* F1-Score
* Classification Report

These metrics help understand not only how many predictions are correct, but also the types of mistakes made by the model.

---

## 💡 Model Interpretation

The Logistic Regression coefficients are analysed to understand how different features are associated with churn risk in this dataset.

The notebook highlights:

* **Monthly Spending:** higher spending is associated with lower churn risk.
* **Complaints:** more complaints are associated with higher churn risk.
* **Age:** shows a smaller relationship with churn compared with the other features.

These relationships are observations from this dataset and should not automatically be treated as causal conclusions.

---

## 📋 Business Output

The project creates a final **SmartKart Customer Churn Risk Report** containing:

* Customer ID
* Age
* Monthly Spending
* Complaints
* Actual Churn
* Predicted Churn
* Churn Probability
* Risk Label

The risk labels are:

```text
Likely to Churn
Not Likely to Churn
```

The report is sorted by churn probability so that higher-risk customers appear first.

The final output is saved as:

```text
smartkart_churn_risk_report.csv
```

---

## 🏢 Business Application

The model can support SmartKart's customer retention process.

### Traditional Process

```text
Customer Data
      ↓
Manual Analysis
      ↓
Identify At-Risk Customers
      ↓
Retention Action
```

### ML-Assisted Process

```text
Customer Data
      ↓
ML Churn Prediction
      ↓
Churn Probability
      ↓
Risk Classification
      ↓
Retention Team Review
      ↓
Customer Retention Action
```

Possible business actions include:

* Sending retention offers
* Following up with high-risk customers
* Investigating frequent complaints
* Improving customer support
* Protecting high-value customer relationships

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Logistic Regression

---

## 📁 Project Structure

```text
smartkart-customer-churn-prediction/
│
├── SmartKart_Churn_Prediction_ML_Pipeline.ipynb
├── smartkart_churn_risk_report.csv
└── README.md
```

If included inside a larger portfolio:

```text
bba-ai-ml-portfolio/
└── part-a/
    └── day03-supervised-learning/
        ├── SmartKart_Churn_Prediction_ML_Pipeline.ipynb
        └── smartkart_churn_risk_report.csv
```

---

## ▶️ How to Run

1. Open the notebook in **Google Colab**.
2. Upload `SmartKart_dirty_100_rows.csv`.
3. Run the cells from top to bottom.
4. Review the data-cleaning and preprocessing outputs.
5. Train the Logistic Regression model.
6. Check the evaluation metrics.
7. Review the feature coefficients.
8. Generate the final churn risk report.
9. Download `smartkart_churn_risk_report.csv`.

---

## 📚 Key Concepts Learned

* Data Collection
* Data Inspection
* Data Cleaning
* Missing Value Handling
* Duplicate Removal
* Outlier Detection
* IQR Method
* Feature Selection
* Target Variable
* Train-Test Split
* Stratification
* Feature Standardisation
* Logistic Regression
* Classification
* Confusion Matrix
* Accuracy
* Precision
* Recall
* F1-Score
* Model Interpretation
* Churn Prediction
* Business Decision Support

---

## 🎓 Academic Context

**Course:** Introduction to AI & ML
**Program:** BBA AI/ML
**Institution:** Chitkara Business School
**CLO:** CLO02 — Apply data preprocessing, feature selection and ML models to business scenarios and evaluate performance using appropriate metrics.

---

## 🚀 Key Learning

This project demonstrates how Machine Learning can transform **raw and messy business data into actionable insights**.

Instead of only building a prediction model, the project connects the complete ML workflow with a real business problem — **customer retention and churn management**.

---

## 📌 Project Status

**Completed — End-to-End ML Pipeline**

The notebook covers the complete workflow from raw customer data to a business-ready churn risk report.
