Predicting Life Satisfaction: A Machine Learning Approach
Overview
This project aims to identify the strongest predictors of life satisfaction using data from the National Health Interview Survey (NHIS) 2023. By leveraging machine learning techniques, the analysis uncovers how various factors such as physical health, mental well-being, and social relationships influence overall life satisfaction.

Background
Understanding the determinants of life satisfaction is crucial for policymakers, healthcare providers, and individuals aiming to improve well-being. While numerous studies have explored this topic, this project utilizes recent data and advanced machine learning models to provide updated insights.

Data Source
The analysis is based on the 2023 National Health Interview Survey (NHIS), conducted by the National Center for Health Statistics (NCHS). The NHIS is a principal source of information on the health of the civilian non-institutionalized population of the United States, collecting data on a broad range of health topics through personal household interviews.

Key Features of the NHIS 2023 Data:

Sample Size: The survey includes responses from thousands of individuals, providing a comprehensive overview of the nation's health.
Content: Data encompasses various health measures, including physical health status, mental health indicators, healthcare access, and sociodemographic information.
Accessibility: Public-use data files and documentation are available for researchers and the public.
For more detailed information, refer to the NHIS 2023 Questionnaires, Datasets, and Documentation: https://www.cdc.gov/nchs/nhis/documentation/2023-nhis.html

Methodology
The project follows these steps:

Data Preprocessing:
Handling missing values.
Scaling features to ensure uniformity across variables.

Feature Selection:
Several feature selection techniques were tested, including correlation-based filtering, recursive feature elimination (RFE), and Lasso Regression.
RFECV (Recursive Feature Elimination with Cross-Validation) was ultimately selected as it provided the most stable and best-performing feature subset.

Model Development:
Training multiple machine learning models, including Random Forest, XGBoost, and Logistic Regression (baseline).
Performing hyperparameter tuning using RandomizedSearchCV to optimize model performance.

Model Evaluation:
Assessing models based on accuracy, precision, recall, and F1-score.
Addressing class imbalance using techniques like KMeansSMOTE.

Interpretation:
Employing SHAP (SHapley Additive Explanations) values to interpret feature importance and understand the impact of each predictor on life satisfaction.
Key Findings
The analysis reveals that:

Physical Health: Self-reported health status is the strongest predictor of life satisfaction. Individuals reporting better health tend to have higher satisfaction levels.

Mental Health: Frequency of depressive and anxiety symptoms significantly impacts life satisfaction. Higher frequencies are associated with lower satisfaction.

Marital Status: Being married or in a committed relationship correlates with higher life satisfaction compared to being single, divorced, or widowed.

Financial Concerns: Worrying about medical bills negatively affects life satisfaction, though its impact is less pronounced than health and relationship factors.

Social Engagement: Participation in volunteer activities and social interactions contributes positively to life satisfaction.
