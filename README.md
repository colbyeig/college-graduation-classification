# Student Enrollment Prediction

This repository contains code for a binary classification project that predicts whether a student will enroll or drop out based on various features. The project involves data preprocessing, feature engineering, dimensionality reduction, and logistic regression modeling. 

## Data
The data is loaded from a CSV file named `student.csv`. It contains information about students, including their demographics, prior qualifications, parents' occupations and salaries, and various other attributes.

### Data Summary
- Number of samples: 4424
- Number of features: 34
- Data types: float64 (5), int64 (29), object (1)

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
2. **Visualization**: We visualize the dataset using PCA.

## Model
1. **Logistic Regression**: We train a logistic regression model with different numbers of features.
2. **Hyperparameter Selection**: We apply 10-fold cross-validation to select the best hyperparameter.
3. **Performance Evaluation**: We evaluate the model's performance using accuracy, recall, precision, F1-score, and Matthews correlation coefficient (MCC).
4. **Learned Model Parameters**: We visualize the learned model parameters.

## Results
- The model's performance improves as the number of features increases.
- With 34 features, the model achieves an accuracy of 91.2%, recall of 95.8%, precision of 91.2%, F1-score of 93.5%, and MCC of 0.803.

For more details on the project, please refer to the code provided in this repository.

---

*Note: This README is a summary based on the code provided. Additional sections or details may be necessary depending on the context and purpose of your repository.*
