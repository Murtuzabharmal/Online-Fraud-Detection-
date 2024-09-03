# Online-Fraud-Detection-
Online Fraud Detection
Overview

This project focuses on detecting fraudulent online payment transactions using various machine learning models. Given the rising threat of online fraud, developing accurate models to detect fraudulent activities is crucial. The project leverages the "Online Payment Fraud Detection" dataset to build and evaluate multiple models, including Logistic Regression, Random Forest, and XGBoost, aiming to optimize performance and accuracy.

Dataset

The dataset used in this project is the Online Payment Fraud Detection dataset, which can be found on Kaggle. The dataset contains transaction records with the following features:

step: Time step for each transaction (hours elapsed).

type: Type of transaction (e.g., CASH_OUT, PAYMENT).

amount: The amount of the transaction.

nameOrig: Customer ID who initiated the transaction.

oldbalanceOrg: Initial balance before the transaction.

newbalanceOrig: New balance after the transaction.

nameDest: Recipient ID of the transaction.

oldbalanceDest: Recipient's initial balance before the transaction.

newbalanceDest: Recipient's new balance after the transaction.

isFraud: Fraudulent transaction indicator (target variable).

isFlaggedFraud: Flag for high-value fraud.

Data Preprocessing

Data preprocessing was performed to clean and prepare the dataset for modeling:

Dropping Unnecessary Columns: The isFlaggedFraud column was dropped as it had limited relevance to the prediction task.

Code:
raw_df.drop('isFlaggedFraud', axis=1, inplace=True)

Handling Missing Values: The dataset was checked for missing values, and appropriate measures were taken. In this case, the dataset was complete with no missing values.

Encoding Categorical Variables: The type column was encoded using LabelEncoder to convert the categorical transaction types into numerical values for model compatibility.

Splitting the Dataset: The dataset was split into training, validation, and test sets using an 80-20 split ratio for training/validation and testing, with a 75-25 split between training and validation.

Feature Scaling: Numerical features were scaled using StandardScaler to standardize the feature values for better model performance.

Feature Engineering
To improve the model's performance, feature engineering was applied to the dataset. This included generating new features, transforming existing features, and selecting the most relevant features.

New Features: Potentially useful new features were created based on domain knowledge and data analysis (if any).

Feature Selection: The most relevant features were selected using techniques like VarianceThreshold or SelectKBest to improve the model's efficiency and accuracy.

Modeling
Multiple models were built and evaluated to identify the best-performing model for fraud detection:

Logistic Regression:

Logistic Regression was the first model applied due to its simplicity and interpretability

Random Forest:

Random Forest, a robust ensemble model, was applied with varying numbers of estimators to enhance prediction accuracy.

XGBoost:

XGBoost, known for its high performance, was used with different configurations to optimize prediction results.

Model Evaluation
The models were evaluated using the following metrics:

Accuracy Score: Measures the ratio of correctly predicted instances to the total instances.

Confusion Matrix: Shows the performance of the model in terms of true positives, true negatives, false positives, and false negatives.

Results
Logistic Regression: Provided baseline performance with moderate accuracy.

Random Forest: Improved the accuracy significantly due to its ensemble nature.

XGBoost: Delivered the highest accuracy and performance, proving to be the best model for this task.

Conclusion
This project successfully developed and evaluated multiple machine learning models for detecting online payment fraud. After preprocessing the data and experimenting with different models, the XGBoost model emerged as the most effective, achieving an accuracy of 89%. This result demonstrates the model's strong capability to identify fraudulent transactions in the dataset. The project highlights the importance of choosing the right features, scaling techniques, and model configurations to optimize performance. Future work could involve further tuning of the XGBoost model, exploring deep learning approaches, or applying the model to real-world data to assess its practical effectiveness.

![image](https://github.com/user-attachments/assets/f4144bb7-0e97-4eed-80cf-e00c0abf3347)


Link: https://colab.research.google.com/drive/1KtjwiwPRQYnPLggAkRwmvy-v1yAecV8L#scrollTo=hAZptQ38jcBo





