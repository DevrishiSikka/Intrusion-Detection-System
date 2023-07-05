# Network Intrusion Detection System

This project implements a Network Intrusion Detection System (NIDS) using machine learning techniques to classify network traffic into different attack categories. The goal is to detect and identify various types of network intrusions, such as Denial of Service (DoS), Probe, Remote to Local (R2L), and User to Root (U2R) attacks.

## Dataset

The project utilizes a labeled network traffic dataset for training and evaluation. The dataset contains features extracted from network packets, including protocol information, connection attributes, and statistical measures.

## Feature Engineering and Preprocessing

The following preprocessing steps were performed on the dataset:

1. Data Cleaning: The dataset was checked for missing values and any necessary cleaning operations were performed.

2. Feature Scaling: The dataset was split into separate dataframes for each attack category. StandardScaler was applied to standardize the features within each category.

3. Feature Selection: Two feature selection techniques were applied:

   - Univariate Feature Selection (ANOVA F-test): SelectPercentile was used to select a percentage of the highest-scoring features based on ANOVA F-values.
   
   - Recursive Feature Elimination (RFE): DecisionTreeClassifier was employed as the estimator for RFE to recursively eliminate less important features.

## Classification Model

A Decision Tree Classifier was chosen as the classification model for its interpretability and ability to handle both numerical and categorical features. The classifier was trained on the selected features from each attack category.

## Results

The performance of the model was evaluated using appropriate metrics such as accuracy, precision, recall, and F1-score. The model's ability to classify network traffic into different attack categories was assessed and the results were analyzed.

## Conclusion

The Network Intrusion Detection System demonstrated promising results in classifying network traffic and detecting various types of network intrusions. The use of feature selection techniques and a decision tree classifier contributed to the accurate identification of attack categories.
