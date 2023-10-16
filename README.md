# Student Enrollment Prediction

1. [Introduction](#introduction)
2. [Data](#data)
3. [Preprocessing](#preprocessing)
4. [Dimensionality Reduction](#dimensionality-reduction)
5. [Model](#model)
6. [Results](#results)
7. [Data Source](#data-source)

## Introduction
This repository contains code for a binary classification project that predicts whether a student will enroll or drop out based on various features. The project involves data preprocessing, feature engineering, dimensionality reduction, and logistic regression modeling.

## Data

The data used in this project is sourced from Kaggle and the original publication:

- **Data Source (Kaggle)**: The dataset can be found on Kaggle at [Predict Students' Dropout and Academic Success](https://www.kaggle.com/datasets/naveenkumar20bps1137/predict-students-dropout-and-academic-success).

- **Original Publication**: Realinho, Valentim, et al. published the data in their research paper titled "Predicting Student Dropout and Academic Success" in the journal Data, Volume 7, Issue 11, in 2022. You can access the original publication at [https://doi.org/10.3390/data7110146](https://doi.org/10.3390/data7110146).

The dataset contains information about students, including their demographics, prior qualifications, parents' occupations and salaries, and various other attributes.

### Data Summary
- Number of samples: 4424
- Number of features: 34

## Preprocessing
1. **Checking for Data Types**: We begin by checking for numerical and categorical data types.
2. **Missing Values**: There are no missing values in the dataset.
3. **Encoding the Target**: We encode the target variable ('Target') as '1' for 'Graduate' and '0' for 'Dropout'.
4. **Reverse Processing Prior Education**: We reverse preprocess prior education, combining and ordinal encoding.
5. **Reverse Processing Mother's and Father's Occupations**: We map them to mean salaries in Portugal.
6. **Visualization**: We visualize mother's and father's salaries through histograms.
7. **Standardization**: We standardize salary features.

## Dimensionality Reduction
1. **Principal Component Analysis (PCA)**: We use PCA to reduce the number of features.
2. **Visualization**: We visualize the Eigen Values of the dataset using a scree plot.

## Model
1. **Logistic Regression**: We train a logistic regression model with different numbers of features using PCA.
2. **Hyperparameter Selection**: We apply 10-fold cross-validation to select the best hyperparameter.
3. **Performance Evaluation**: We evaluate the model's performance using accuracy, recall, precision, F1-score, and Matthews correlation coefficient (MCC).
4. **Learned Model Parameters**: We visualize the learned model parameters.

## Results
- The model's performance improves as the number of features increases.
- The model likely way overfit the Learned Model Parameters for the 34 feature datasset.
- International students are much more likely to dropout than their domestic peers.
- Students who applied during the Early Decision/Early Action window are much more likely to graduate than their Regular Decision / Late Enroll peers.

## TO DO
- Add visualizations comparing model performance for each model with a different number of features.
- Implement a 'Confusion Matrix' visual from an external library
- Complete a Multiple Kernel Learning Analysis where features are grouped together and Learned Model Parameters can be better visualized

For more details on the project, please refer to the code provided in this repository.

---
