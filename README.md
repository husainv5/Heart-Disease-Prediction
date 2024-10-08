# Heart Disease Classification Project

This project aims to predict the presence of heart disease in individuals using the **Heart Disease UCI dataset**. The prediction model is built using a Random Forest classifier, and the data was cleaned, analyzed, and visualized using Databricks.

## Overview

- **Tools Used:** Databricks, PySpark, SQL, Matplotlib, Seaborn, Scikit-learn
- **Algorithms Used:** Random Forest Classifier
- **Key Visualizations:**
  - Cholesterol distribution by heart disease
  - Confusion Matrix
  - Correlation Heatmap
  - ROC Curve

## Dataset

The dataset used for this project comes from the UCI Machine Learning Repository. It contains various attributes related to heart health, which are used to classify whether an individual has heart disease.

### Columns of Interest:
- **Age**: Patient's age
- **Sex**: Male or Female
- **Resting Blood Pressure**: Blood pressure (in mm Hg) while at rest
- **Cholesterol**: Serum cholesterol level (mg/dL)
- **Fasting Blood Sugar**: Whether fasting blood sugar is > 120 mg/dL
- **Max Heart Rate**: Maximum heart rate achieved during exercise
- **ST Depression**: Depression in the ST segment of the ECG
- **Target (Heart Disease)**: 1 = Heart disease present, 0 = No heart disease

## Notebooks and Files

- **Notebook:** The main notebook (`Heart Disease.ipynb`) contains the full process, including data cleaning, exploratory data analysis (EDA), model training, evaluation, and visualizations.
- **SQL Queries:** SQL was used within Databricks to query, filter, and manipulate data.
- **Model:** A Random Forest Classifier was applied to predict heart disease presence, trained on various features.

## Exploratory Data Analysis (EDA)

To gain insights into the data, several visualizations were created. Here are some key ones:

### Cholesterol Distribution by Heart Disease

![Cholesterol_Distribution](images/Cholesterol_Dist_heart_data.png)
*This histogram compares cholesterol levels between people with and without heart disease.*

- **Explanation**: The plot highlights the distribution of cholesterol levels. Patients without heart disease tend to have a wider spread of cholesterol values, while those with heart disease show higher cholesterol levels concentrated at specific points. Some individuals with heart disease show a cholesterol level of zero, possibly indicating missing or anomalous data.

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix_heart_data.png)
*This confusion matrix shows the breakdown of the model’s predictions: true positives, false positives, true negatives, and false negatives.*

- **Explanation**: The model successfully predicted 60 true negatives and 93 true positives, indicating that it correctly identified patients with and without heart disease in many cases. However, it also resulted in 21 false negatives and 21 false positives, highlighting areas for potential improvement.

### Correlation Heatmap

![Correlation_Heatmap](images/correlation_heatmap_heart_data.png)
*The correlation heatmap shows relationships between variables, where darker colors represent stronger correlations.*

- **Explanation**: Max Heart Rate (MaxHR) and ST Depression (Oldpeak) have stronger correlations with the presence of heart disease than other features. These variables play a crucial role in the classification process.

## Model Performance

The Random Forest classifier was used to predict heart disease. Below are the key performance metrics:

- **Accuracy:** 78.46%
- **Precision:** 78.46%
- **Recall:** 78.46%
- **F1-Score:** 78.46%
- **ROC-AUC Score:** 0.83

- **Explanation**: The model shows balanced precision, recall, and F1-Score, meaning it performs consistently across all evaluation metrics. The ROC-AUC score of 0.83 indicates a good overall performance, with the model being able to distinguish well between positive and negative cases.

## Conclusions and Insights

Through this analysis, it was confirmed that certain features, such as cholesterol, exercise-induced angina, and maximum heart rate, are strongly associated with heart disease. The following key insights were observed:

- **Cholesterol Levels**: Elevated cholesterol levels are a key indicator of heart disease.
- **Max Heart Rate**: Lower maximum heart rates are often associated with heart disease, potentially due to reduced cardiovascular efficiency.
- **Chest Pain Type**: Different types of chest pain, particularly asymptomatic (silent ischemia), have a stronger relationship with heart disease.


## Setup Instructions

### Requirements

- Python 3.x
- PySpark
- Databricks
- Matplotlib, Seaborn
- Scikit-learn

### How to Run the Code

1. Clone the repository:
   ```bash
   git clone https://github.com/husainv5/heart-disease-classification.git
