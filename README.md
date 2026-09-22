# Customer Response Prediction Using Machine Learning

MSc Data Science project applying machine learning, explainable AI (XAI), SHAP and Power BI to predict customer responses to marketing campaigns across the banking and retail sectors.

## 📌 Project Overview

Marketing organisations need to identify customers who are more likely to respond positively to campaigns. This project investigates how machine learning can be used to predict customer responses while also explaining the factors influencing model predictions.

The project analyses 47,451 customer records across two marketing datasets and compares three classification algorithms:

* Logistic Regression
* Random Forest
* XGBoost

The project combines predictive modelling with SHAP-based explainability and Power BI dashboards to translate analytical results into actionable marketing insights.

## 🎯 Objectives

The project aimed to:

1. Analyse customer and campaign characteristics using exploratory data analysis.
2. Develop machine learning models for customer response prediction.
3. Compare model performance using accuracy, precision, recall and F1-score.
4. Address class imbalance using SMOTE.
5. Explain model predictions using SHAP.
6. Develop interactive Power BI dashboards.
7. Translate predictive results into practical marketing insights.

## 📊 Datasets

### Bank Marketing Dataset

* 45,211 records
* 17 variables
* Target: `y` — term-deposit subscription
* Source: Bank Marketing dataset

### Retail Marketing Dataset

* 2,240 records
* 29 variables
* Target: `Response` — campaign response
* Source: Customer Personality Analysis dataset

Raw customer-level datasets are not included in this public repository.

## 🔬 Methodology

The analytical workflow followed these main stages:

```text
Data Collection
      ↓
Exploratory Data Analysis
      ↓
Data Cleaning & Preprocessing
      ↓
Feature Engineering
      ↓
Encoding & Scaling
      ↓
Train/Test Split
      ↓
SMOTE
      ↓
Machine Learning Modelling
      ↓
Model Evaluation
      ↓
SHAP Explainability
      ↓
Power BI Dashboards
      ↓
Marketing Insights
```

### Data Processing

The project included:

* Missing-value assessment
* Duplicate-value assessment
* Categorical variable encoding
* Feature engineering
* Customer tenure calculation for the retail dataset
* Train/test splitting
* Feature scaling for Logistic Regression
* SMOTE applied to the training data to address class imbalance

## 🤖 Machine Learning Models

Three classification algorithms were evaluated:

| Model               | Description                      |
| ------------------- | -------------------------------- |
| Logistic Regression | Baseline classification model    |
| Random Forest       | Ensemble of decision trees       |
| XGBoost             | Gradient boosting ensemble model |

## 📈 Model Performance

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score

| Model               | Dataset |  Accuracy | Precision |    Recall |  F1-score |
| ------------------- | ------- | --------: | --------: | --------: | --------: |
| Logistic Regression | Bank    |     88.5% |     50.8% |     45.6% |     48.1% |
| Random Forest       | Bank    |     90.1% |     58.8% |     51.3% |     54.8% |
| XGBoost             | Bank    |     89.7% |     55.3% |     60.2% |     57.7% |
| Logistic Regression | Retail  |     86.4% |     53.9% |     61.2% |     57.3% |
| Random Forest       | Retail  |     87.3% |     58.9% |     49.3% |     53.7% |
| XGBoost             | Retail  |     88.4% |     62.7% |     55.2% |     58.7% |

The results show different performance patterns across the two datasets. For the bank dataset, XGBoost achieved the highest recall and F1-score, while Random Forest achieved the highest accuracy and precision. For the retail dataset, XGBoost achieved the highest accuracy, precision and F1-score, while Logistic Regression achieved the highest recall.

## 🧠 Explainable AI — SHAP

SHAP (SHapley Additive exPlanations) was used to interpret the XGBoost models and identify the factors contributing to customer response predictions.

### Banking Dataset

Important predictive factors included:

* Call duration
* Previous campaign outcomes
* Days since previous contact
* Contact method
* Campaign month
* Account balance

Call duration was the most influential feature in the bank model. This should be interpreted as a predictive association rather than evidence that longer calls cause customers to subscribe.

### Retail Dataset

Important predictive factors included:

* Recency
* Customer tenure
* Number of teenage children
* Education
* Marital status
* Gold expenditure
* Store purchases
* Meat expenditure
* Wine expenditure
* Income

The retail model therefore placed greater emphasis on customer demographics and historical purchasing behaviour.

## 📊 Power BI Dashboards

Three interactive Power BI dashboards were developed to communicate the analytical findings.

### Executive Dashboard

Provides a high-level overview of customer characteristics, campaign responses and key marketing indicators.

![Executive Dashboard](powerbi/Executive_Dashboard.png)

### Predictive Analytics Dashboard

Presents predictive modelling outputs and customer response analysis.

![Predictive Analytics Dashboard](powerbi/Predictive_Analytics_Dashboard.png)

### Marketing Strategy Dashboard

Combines customer segmentation, campaign performance and purchasing behaviour to support marketing analysis.

![Marketing Strategy Dashboard](powerbi/Marketing_Strategy_Dashboard.png)

## 💡 Business Insights

The analysis demonstrates how predictive analytics can support marketing decision-making by:

* Identifying customer characteristics associated with campaign responses
* Supporting customer segmentation
* Informing targeted marketing campaigns
* Identifying important behavioural and demographic predictors
* Supporting campaign monitoring through interactive dashboards
* Connecting predictive model outputs with explainable insights

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* imbalanced-learn / SMOTE
* SHAP
* Matplotlib
* Seaborn
* Jupyter Notebook
* Microsoft Power BI
* GitHub

## 📁 Repository Structure

```text
Customer-Response-Prediction-ML/
│
├── data/
│   └── README.md
│
├── figures/
│   ├── logistic_retail_confusion_matrix.png
│   ├── random_forest_bank_confusion_matrix.png
│   ├── random_forest_retail_confusion_matrix.png
│   ├── xgboost_bank_confusion_matrix.png
│   └── xgboost_retail_confusion_matrix.png
│
├── notebooks/
│   └── Marketing_Campaign_Prediction.ipynb
│
├── powerbi/
│   ├── Executive_Dashboard.png
│   ├── Predictive_Analytics_Dashboard.png
│   └── Marketing_Strategy_Dashboard.png
│
├── results/
│   ├── model_performance.csv
│   └── README.md
│
└── README.md
```

## 🔍 Project Outputs

The repository contains:

* Complete analytical notebook
* Model performance results
* Confusion matrices
* Power BI dashboard screenshots
* Project documentation

Customer-level raw datasets are excluded from the repository.

## 🎓 Academic Context

This project was completed as part of an MSc Data Science dissertation at the University of Sheffield.

Project focus: Machine Learning, Marketing Analytics, Explainable AI and Business Intelligence.

## 👤 Author

Thomas Felix Noonoo

MSc Data Science | Data Analytics | Machine Learning | Business Intelligence

