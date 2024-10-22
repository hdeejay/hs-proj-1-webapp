Bank Customer Churn Prediction

This project aims to predict whether a customer will churn (leave the bank) using machine learning models. The process involves data visualization, pre-processing, training/testing models, and improving model performance.

Libraries Used

pandas: Data manipulation
matplotlib: Data visualization
seaborn: Enhanced data visualization on top of matplotlib
scikit-learn: Machine learning models, train-test splitting, and evaluation
XGBoost: For gradient boosting
Dataset

The dataset is sourced from the Kaggle Churn for Bank Customers dataset.

Steps Overview

1. Data Visualization
Churn Distribution: A countplot visualizing the number of churned vs. non-churned customers.
Age vs Credit Score: A scatterplot exploring the relationship between credit score, age, and customer churn.
2. Preprocessing
Separated the target variable (churn) and features.
Removed irrelevant columns like customer ID and row numbers.
Handled missing values using .dropna().
Applied one-hot encoding for categorical variables like Geography and Gender.
3. Data Splitting and Scaling
Split the data into 80% training and 20% testing.
Scaled features to ensure uniform influence across all variables using StandardScaler().
4. Model Training and Evaluation
Trained multiple models, including:
Logistic Regression
Decision Tree
Random Forest
XGBoost
Naive Bayes
K-Nearest Neighbors
Support Vector Machine (SVM)
Evaluated each model's accuracy, precision, recall, and F1 score using the classification_report from sklearn.
5. Feature Engineering
Added new features like Customer Lifetime Value (CLV), Age Group, and Tenure-to-Age ratio.
Applied further one-hot encoding for categorical data.
6. Improving the Model
SMOTE: Balanced the dataset using synthetic data generation for the minority class.
Ensemble Methods: Used a Voting Classifier for combining predictions from multiple models (Random Forest, XGBoost, and SVM).
Results

The Random Forest model achieved the highest accuracy, while XGBoost had the highest recall for identifying churners.
The Voting Classifier provided the best overall performance, with improved recall on churners.
Conclusion

This project covers data preprocessing, feature engineering, training/testing models, and improving model performance using advanced techniques like SMOTE and Ensemble methods. The models are saved as .pkl files for further use.
