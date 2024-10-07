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

This plot shows the distribution of cholesterol levels for patients with and without heart disease. It indicates that cholesterol is an important feature for distinguishing between the two groups.

### Confusion Matrix

The confusion matrix evaluates the performance of the Random Forest classifier. It displays the true positive and true negative predictions, as well as any misclassifications.

### Correlation Heatmap

The correlation heatmap highlights the relationships between the different features. Features that are strongly correlated with heart disease can be identified.

### ROC Curve

The ROC curve illustrates the true positive rate versus the false positive rate for the Random Forest classifier, with an Area Under the Curve (AUC) score to measure model performance.

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
