# Probability Forecasting for Flu Vaccination: XYZ and Seasonal

## Overview

This project aims to predict the likelihood of individuals receiving two types of flu vaccines: XYZ flu vaccine and seasonal flu vaccine. The prediction is based on various demographic, behavioral, and opinion-based features of respondents.

### Problem Statement

The goal is to build predictive models that estimate the probability of individuals getting vaccinated against XYZ flu and seasonal flu. This involves predicting two binary outcomes:
- `xyz_vaccine`: Whether a respondent received the XYZ flu vaccine (0 = No, 1 = Yes).
- `seasonal_vaccine`: Whether a respondent received the seasonal flu vaccine (0 = No, 1 = Yes).

### Data Description

- **Features**: The dataset includes demographic information (age group, education, race, etc.), behavioral factors (antiviral medication use, handwashing habits, etc.), opinions about vaccine effectiveness and risks, and other relevant attributes.
- **Labels**: Binary labels indicating whether respondents received each type of flu vaccine.

### Evaluation Metric

Performance will be evaluated using the area under the receiver operating characteristic curve (ROC AUC) for each vaccine prediction. The mean ROC AUC score across both predictions will determine the overall model performance.

## Repository Structure

- `data/`: Contains training and test datasets (`training_set_features.csv`, `training_set_labels.csv`, `test_set_features.csv`).
- `notebooks/`: Jupyter notebooks for data exploration, preprocessing, modeling, and evaluation.
- `scripts/`: Python scripts for specific tasks like data preprocessing, model training, and prediction.
- `README.md`: Overview of the project, problem statement, dataset description, evaluation metric, and repository structure.

## Approach

1. **Data Preprocessing**:
   - Handling missing values.
   - Encoding categorical variables.
   - Feature engineering if necessary.

2. **Exploratory Data Analysis (EDA)**:
   - Understanding distributions of features.
   - Exploring relationships between features and target variables.

3. **Modeling**:
   - Training separate logistic regression models for `xyz_vaccine` and `seasonal_vaccine`.
   - Evaluating model performance using ROC AUC score.

4. **Evaluation**:
   - Assessing model performance on the validation set.
   - Predicting probabilities on the test set for submission.

5. **Visualization**:
   - Plotting ROC curves to visualize model performance.

## Requirements

- Python 3.x
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn

