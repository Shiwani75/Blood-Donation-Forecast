# Blood Donation Forecast
## Overview 
This repository contains a machine learning model aimed at predicting blood donation behavior. The task involves classifying individuals based on whether they will donate blood in the future using various features from the dataset. The models employed include Random Forest Classifier and Logistic Regression. Model performance is evaluated using AUC (Area Under the Curve) and ROC (Receiver Operating Characteristic) curve metrics.


## Table of Contents
- [Project Description](#project-description)
- [Model Building Process](#model-building-process)
- [Prerequisites](#prerequisites)
- [Installation Instructions](#installation-instructions)
- [Data](#data)
- [Model Training](#model-training)
- [Evaluation](#evaluation)


## Project Description

The goal of this project is to predict whether an individual will donate blood based on various features such as age, number of donations, and blood donation frequency. The dataset contains information about people’s blood donation history and their donation behavior.


## Model Building Process

The following steps outline the model-building process:

### 1. Load and Preprocess Data:
- The training and test datasets are loaded using pandas.
- We drop unnecessary columns and handle any missing values (if applicable).

### 2. Feature Engineering:
- Feature normalization is performed, particularly on the "Monetary (c.c. blood)" column to reduce variance, improving the model's performance.

### 3. Model Training:
- *Random Forest Classifier* is trained with hyperparameter tuning using GridSearchCV to optimize the model's performance.
- *Logistic Regression* is trained as a comparative model.

### 4. Model Evaluation:
- Both models' performance is evaluated using the *AUC* (Area Under the Curve) score, which is calculated using the roc_auc_score function.
- The models are compared based on their AUC scores and visualized using a bar chart.

### 5. ROC Curve:
- The *ROC curves* for both models are plotted to visualize the trade-off between the true positive rate and false positive rate.
## Data
The project uses three CSV files for training and testing the models:

- blood-train.csv - The training dataset with features and labels.
- blood-test.csv - The test dataset used to predict blood donation behavior.
- blood-format.csv - A file detailing the format for the datasets (usually contains column information).

### Key Features:
- *Random Forest Classifier*: A robust ensemble learning model used to classify blood donation outcomes.
- *Logistic Regression*: A statistical method used for binary classification.
- *AUC Score*: The model’s performance is evaluated using the ROC-AUC score, which is particularly useful for imbalanced classes.

## Prerequisites

Before running the project, you need to install the following libraries:

- pandas: For data manipulation
- numpy: For numerical operations
- scikit-learn: For machine learning algorithms
- matplotlib: For data visualization
- seaborn: For enhanced data visualization

Install them using the following command:

```bash
pip install pandas 
pip install numpy 
pip install scikit-learn 
pip install seaborn
pip install matplotlib
