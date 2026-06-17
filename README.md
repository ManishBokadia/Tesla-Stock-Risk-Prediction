# Tesla Stock Risk Prediction Using Machine Learning

## Project Overview

This project analyzes Tesla (TSLA) stock market data and builds machine learning models to predict the next day's stock risk category.

The project uses historical Tesla stock data obtained from Yahoo Finance and applies Exploratory Data Analysis (EDA), Z-Score based risk classification, and machine learning algorithms to predict future risk levels.

Risk Categories:
- Low Risk
- Medium Risk
- High Risk

---

## Problem Statement

Investors and analysts need a way to identify potential stock risk levels based on historical market behavior.

The objective of this project is to classify Tesla stock observations into risk categories and build a predictive model capable of forecasting the next day's risk class.

---

## Dataset

Source: Yahoo Finance

Features Used:

- Open_TSLA
- High_TSLA
- Low_TSLA
- Close_TSLA
- Volume_TSLA

Total Records: 238

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

### 1. Data Understanding
- Checked dataset structure
- Verified data types
- Examined summary statistics

### 2. Data Quality Checks
- Missing Value Analysis
- Duplicate Check

### 3. Distribution Analysis
- Histogram of Tesla Closing Prices

### 4. Correlation Analysis
- Correlation Heatmap
- Relationship between stock price variables

### 5. Outlier Detection
- Volume Boxplot
- Identification of unusual trading activity

---

## Key Findings from EDA

- The dataset contained 238 observations with no missing values.
- Tesla closing prices ranged approximately between 220 and 470.
- Open, High, Low and Close prices showed extremely strong positive correlations.
- Volume showed a moderate negative correlation with stock prices.
- Outliers were observed mainly in trading volume, which is common in stock market datasets.

---

## Risk Classification

Z-Score analysis was used to classify stock observations into risk categories.

### Z-Score Formula

Z = (X - Mean) / Standard Deviation

### Risk Categories

| Risk Class | Condition |
|------------|-----------|
| Low | Z-Score < -1 |
| Medium | -1 ≤ Z-Score ≤ 1 |
| High | Z-Score > 1 |

### Risk Distribution

| Risk Class | Count |
|------------|--------|
| Medium | 136 |
| High | 57 |
| Low | 45 |

---

## Target Variable Creation

The target variable was created by shifting the Risk Class column by one day.

This allows the model to learn from today's stock information and predict tomorrow's risk category.

---

## Machine Learning Models

The following classification algorithms were implemented and evaluated:

1. K-Nearest Neighbors (KNN)
2. Decision Tree
3. Support Vector Machine (SVM)
4. Random Forest

---

## Model Performance

| Model | Accuracy |
|---------|---------|
| SVM | 91.67% |
| KNN | 89.58% |
| Random Forest | 89.58% |
| Decision Tree | 85.42% |

---

## Best Model

### Support Vector Machine (SVM)

Performance:

- Accuracy: 91.67%
- Highest performing model
- Perfect classification of High Risk observations
- Strong overall precision and recall

Therefore, SVM was selected as the final prediction model.

---

## Project Findings

1. Tesla stock prices exhibit strong relationships among Open, High, Low and Close prices.
2. Trading volume behaves differently from price variables and shows weaker correlation.
3. Z-Score successfully categorized stock observations into meaningful risk classes.
4. Machine learning models were able to learn patterns from historical stock data.
5. SVM achieved the highest prediction accuracy of 91.67%.
6. The final model can be used to predict future Tesla stock risk categories.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-Learn
- Joblib
- Google Colab

---

## Repository Contents

- Tesla_Stock_Risk_Prediction.ipynb
- tesla_risk_model.pkl
- scaler.pkl
- label_encoder.pkl
- README.md

---


## Author

Tesla Stock Risk Prediction Using Machine Learning

Manish Bokadia
