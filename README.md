# 🌧️ Weather Forecast Classifier

## Project Status

[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-v0.24+-orange)](https://scikit-learn.org/stable/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 🎯 Project Goal

This project details a machine learning approach to **binary classification** for weather forecasting. The primary objective is to develop and evaluate predictive models to accurately forecast the likelihood of **Rain** (`1`) or **No Rain** (`0`) based on atmospheric conditions.

The analysis compares a linear model (**Logistic Regression**) against an ensemble model (**Random Forest Classifier**) to identify the most robust and accurate predictor.

---

## 📊 Key Findings

### 1. Model Performance Summary

The models were rigorously evaluated using the **ROC AUC score** and **F1-score**, which are superior metrics given the **severe class imbalance** (approx. 7:1 ratio of "No Rain" to "Rain") observed in the dataset.

| Model | ROC AUC Score | F1-Score (Weighted Avg) | Key Insight |
| :--- | :--- | :--- | :--- |
| **Random Forest Classifier** | **1.0000** | **1.00** | Achieved **perfect discrimination** on the test set, demonstrating exceptional non-linear modeling capability. |
| **Logistic Regression** | **0.9649** | **0.92** | A high-performing linear model, but was less effective than Random Forest at correctly distinguishing the minority 'Rain' class. |

### 2. Feature Importance

Feature importance analysis confirmed the meteorological intuition, with the following variables being the most critical predictors:

| Feature | Predictive Influence |
| :--- | :--- |
| **Humidity** | Highest positive influence; essential for predicting precipitation. |
| **Cloud Cover** | Second strongest positive predictor. |
| **Temperature** | Strong **negative correlation**; higher temperatures strongly reduce the probability of rain. |

### 3. Data Insights

Visualizations (Bar Graphs, Boxplots, and Heatmaps) confirmed the following data properties:
* The target variable exhibits a **severe class imbalance**.
* The data is **clean** with no significant outliers requiring removal.
* The **Correlation Heatmap** validated the strong linear relationships between Humidity, Cloud Cover, Temperature, and the target variable.

---

## 🛠️ Technologies and Libraries

The project was developed using the following standard Python data science libraries:

* **Python 3.x**
* `Pandas` (Data manipulation)
* `NumPy` (Numerical operations)
* `Scikit-learn` (Modeling and evaluation)
* `Matplotlib` / `Seaborn` (Visualization)

---

## 🚀 Getting Started

Follow these steps to run the analysis locally.

### Prerequisites

Install all required Python libraries using pip:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

git clone [https://github.com/sreekarnati/Weather_Forecast_Prediction](https://github.com/sreekarnati/Weather_Forecast_Prediction)
cd Weather_Forecast_Prediction

📂 Repository Structure

├── Weather_Forecast.ipynb    # Main Jupyter Notebook with all analysis steps
├── dataset/                  
│   └── weather_forecast_data.csv  # Required input data file
└── README.md                 # Project documentation


