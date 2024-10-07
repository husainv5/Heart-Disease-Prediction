# Heart Disease Classification Project

This project aims to predict the presence of heart disease in individuals using the **Heart Disease UCI dataset**. The prediction model is built using a Random Forest classifier, and the data was cleaned, analyzed, and visualized using Databricks.

## Overview

- **Tools Used:** Databricks, PySpark, SQL, Matplotlib, Seaborn, Scikit-learn
- **Algorithms Used:** Random Forest Classifier
- **Key Plots:**
  - Cholesterol distribution by heart disease
  - Confusion Matrix
  - Correlation Heatmap
  - ROC Curve

## Dataset

The dataset used for this project comes from the UCI Machine Learning Repository. It contains various attributes related to heart health and habits, which are used to classify whether an individual has heart disease.

- **Columns of Interest:**
  - Age, Sex, Resting Blood Pressure, Cholesterol, Fasting Blood Sugar, Max Heart Rate, ST Depression, etc.

## Notebooks and Files

- **Notebook:** The main notebook (`Heart Disease.ipynb`) contains the entire code for data cleaning, model training, and visualization.
- **SQL Queries:** SQL is used to initially query and manipulate data in Databricks.
- **Random Forest Classifier:** The machine learning model used to make predictions.

## Visualizations

### Cholesterol Distribution by Heart Disease

![Cholesterol_Distribution](images/Cholesterol_Dist_heart_data.png)
*This plot shows the distribution of cholesterol levels for patients with and without heart disease. It indicates that cholesterol is an important feature for distinguishing between the two groups.*

This is a histogram comparing cholesterol levels between people with and without heart disease. The x-axis represents cholesterol levels, while the y-axis shows the count of individuals.

There is a clear distinction between cholesterol levels for individuals with and without heart disease. It shows that individuals with no heart disease (blue bars) are spread across a range of cholesterol values, while a significant number of individuals with heart disease (orange bars) have a cholesterol level of 0. This suggests either missing data or a subgroup of patients with distinct cholesterol characteristics.

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix_heart_data.png)
*Confusion matrix showcasing the true positives, false negatives, and false positives in heart disease classification.*

A confusion matrix that compares actual labels (True Labels) with predicted labels from the machine learning model. It measures how well the model classifies individuals as having heart disease (1) or not (0).

The model predicted 60 true negatives (correctly predicted as not having heart disease), 21 false negatives (incorrectly predicted as not having heart disease), 21 false positives (incorrectly predicted as having heart disease), and 93 true positives (correctly predicted as having heart disease). This indicates a relatively good performance with a slight bias toward predicting heart disease.

### Correlation Heatmap

![Correlation_Heatmap](images/correlation_heatmap_heart_data.png)

This heatmap shows the correlation between different features in the dataset, including the target variable (HeartDisease). The intensity of color represents the strength and direction of the correlation, with darker shades indicating stronger correlations.

The heatmap shows that features like MaxHR (Maximum Heart Rate) and Oldpeak have relatively stronger correlations with heart disease (-0.4 and 0.4 respectively). Age and RestingBP, on the other hand, do not show strong correlations with heart disease.

## Model Performance

The Random Forest model was evaluated using several metrics:
- **Accuracy:** 0.78
- **Precision, Recall, F1-Score:**  0.78 , 0.78,  0.78
- **AUC (ROC Curve):** 0.83

## Setup Instructions

### Requirements

- Python 3.x
- PySpark
- Matplotlib
- Seaborn
- Scikit-learn
- Databricks (for cloud-based notebook and SQL)

### How to Run the Code

1. Clone the repository:
   ```bash
   git clone https://github.com/husainv5/heart-disease-classification.git
