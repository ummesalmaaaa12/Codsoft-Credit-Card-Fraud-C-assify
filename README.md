# Codsoft-Credit-Card-Fraud-C-assify
A machine learning project for detecting credit card fraud using real-world transaction data and the XGBoost algorithm.
# Credit Card Fraud Detection – Machine Learning Project

This repository contains a machine learning project developed during my internship at CodSoft. The aim of this project is to detect fraudulent credit card transactions using a supervised classification approach. It demonstrates the complete data science workflow, including data preprocessing, feature engineering, model training, and evaluation using real-world transaction data.

## Project Objective

The goal is to build a model capable of classifying credit card transactions as fraudulent or legitimate based on features such as transaction amount, location, merchant, user demographics, and time-related attributes. Due to the highly imbalanced nature of fraud detection problems, the project focuses on optimizing recall and F1-score to reduce false negatives while maintaining overall reliability.

## Dataset

- Source: [Kaggle - Fraud Detection Dataset](https://www.kaggle.com/datasets/kartik2112/fraud-detection)
- The dataset includes two files: `train.csv` and `test.csv`
- Features include:
  - Transaction information (amount, merchant, category)
  - User profile data (gender, job, city, state)
  - Geographic coordinates (latitude, longitude)
  - Timestamps (Unix time, extracted hour and day)
  - Target label: `is_fraud` (0 = legitimate, 1 = fraudulent)

## Key Steps in the Project

1. Data Exploration
   - Checked data quality, value distributions, and class imbalance
   - Verified no missing values and understood the types and range of features

2. Preprocessing
   - Combined training and testing data for consistent preprocessing
   - Label encoded categorical features such as gender, job, merchant, and category
   - Scaled numerical features to normalize transaction amounts and coordinates

3. Feature Engineering
   - Created additional features like `transaction hour`, `transaction day`, and `user age`
   - Evaluated correlations and relevance of features with the target variable

4. Model Development
   - Implemented XGBoost classifier for its robustness and ability to handle imbalanced data
   - Tuned model parameters and suppressed warnings for categorical compatibility
   - Focused on optimizing recall and F1-score due to the importance of detecting fraud cases

5. Model Evaluation
   - Evaluated using confusion matrix, precision, recall, and F1-score
   - Observed strong model performance in identifying fraud without sacrificing general accuracy

## Challenges Addressed

- **Class Imbalance**: Since fraud cases were rare, special attention was given to evaluation metrics that reflect real-world performance rather than relying solely on accuracy.
- Feature Consistency: Ensured that the same transformations were applied to both training and testing data to avoid leakage or misalignment.
- Model Selection: Gained hands-on experience with XGBoost, including error handling with object-type features and the importance of clean input formatting.

## Tools and Technologies

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn (for internal analysis)

## Outcome

The final model was able to effectively detect fraud with high reliability and meaningful recall. This project demonstrates how machine learning can be used in financial applications to improve fraud detection and risk management. It also highlights the importance of preprocessing, feature design, and metric selection in real-world classification problems.

## Author

Ummesalma Rampurwala  
Machine Learning Intern, CodSoft

---

