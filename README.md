# Predicting Life Satisfaction: A Machine Learning Approach

## Overview  
This project aims to identify the strongest predictors of life satisfaction using data from the National Health Interview Survey (NHIS) 2023. By leveraging machine learning techniques, the analysis uncovers how various factors such as physical health, mental well-being, and social relationships influence overall life satisfaction.

## Background  
Understanding the determinants of life satisfaction is crucial for policymakers, healthcare providers, and individuals aiming to improve well-being. While numerous studies have explored this topic, this project utilizes recent data and advanced machine learning models to provide updated insights.

## Data Source  
The analysis is based on the 2023 National Health Interview Survey (NHIS), conducted by the National Center for Health Statistics (NCHS). The NHIS is a principal source of information on the health of the civilian, non-institutionalized population of the United States, collecting data on a broad range of health topics through personal household interviews.

### Key Features of the NHIS 2023 Data:
- Sample Size: Thousands of individuals, providing a comprehensive overview of national health.
- Content: Covers physical health, mental health indicators, healthcare access, and sociodemographics.
- Accessibility: Public-use data and documentation are available for researchers and the public.

For more information, see the [NHIS 2023 Data & Documentation](https://www.cdc.gov/nchs/nhis/documentation/2023-nhis.html).

## Methodology  

### Data Preprocessing
- Handled missing values.
- Scaled features to ensure uniformity across variables.

### Feature Selection
Several feature selection techniques were tested to identify the best predictors of life satisfaction:
- Spearman’s Correlation – Initial filtering based on monotonic relationships with life satisfaction.
- Recursive Feature Elimination (RFE) – Iteratively removed least important features.
- Lasso Regression (L1 Regularization) – Shrunk less relevant features toward zero.
- RFECV (Recursive Feature Elimination with Cross-Validation) – Selected as the final method due to its stability and performance across models.

### Model Development
- Trained multiple machine learning models, including Random Forest, XGBoost, and Logistic Regression as a baseline.
- Tuned hyperparameters using RandomizedSearchCV to optimize performance.

### Model Evaluation
- Assessed models using accuracy, precision, recall, and F1-score.
- Addressed class imbalance using KMeansSMOTE.

### Interpretation
- Used SHAP (SHapley Additive Explanations) to interpret feature importance and understand the impact of each predictor on life satisfaction.

## Key Findings  

The analysis reveals that:

- Physical Health: Self-reported health status is the strongest predictor of life satisfaction. Individuals reporting better health tend to have higher satisfaction levels.
- Mental Health: Frequent depression and anxiety symptoms strongly correlate with lower life satisfaction.
- Marital Status: Being married or in a committed relationship is linked to higher life satisfaction.
- Financial Concerns: Worrying about medical bills has a negative impact, though it is less significant than health and relationships.
- Social Engagement: Participation in volunteer activities and social interactions contributes positively to life satisfaction.
