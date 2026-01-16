# Student-Performance-Data-Analysis
Project Overview
This project focuses on analyzing student performance data to understand the factors affecting academic success.
The main objective is to build a machine learning model that predicts whether a student will pass or fail, based on behavioral and academic features.
The project follows a complete data science workflow, including data exploration, preprocessing, handling class imbalance, and model evaluation.

Dataset Description
The dataset contains the following features:
* student_id
* weekly_self_study_hours
* attendance_percentage
* class_participation
* grade
* total_score
  
A target variable named pass was created based on the total_score:
1 → Pass (total_score ≥ 60)
0 → Fail (total_score < 60)

Technologies Used:
Python
Pandas & NumPy – Data manipulation
Matplotlib & Seaborn – Data visualization
Scikit-learn – Machine learning
Google Colab
GitHub

Exploratory Data Analysis (EDA):
Checked dataset structure, data types, and summary statistics
Verified that there are no missing values
Visualized score distributions and class imbalance
Observed a highly imbalanced dataset, with significantly more passing students than failing ones

Data Leakage Handling:
During initial modeling, extremely high performance was observed.
This was caused by data leakage, as the target variable (pass) was directly derived from the total_score feature.

Solution:
Removed total_score from the feature set
Ensured that the model learns from independent features only
Achieved more realistic and reliable model performance

Handling Class Imbalance:
Since the dataset is highly imbalanced:
Accuracy alone was not considered sufficient
Class weighting was applied in the Logistic Regression model
Precision, recall, and F1-score were used for evaluation

Model Building:
Algorithm: Logistic Regression
Applied Label Encoding for categorical variables
Used stratified train-test split
Evaluated using confusion matrix and classification report

Model Performance:
After removing data leakage and encoding categorical features:
Accuracy: ~90%
Recall (Fail class): ~99%
The model successfully identifies students at risk of failure
This makes the model suitable for early warning systems in educational settings.

Key Takeaways:
Identified and prevented data leakage
Handled categorical variables and class imbalance
Focused on meaningful evaluation metrics
Built a realistic and interpretable machine learning model

Future Improvements:
Try tree-based models (Random Forest, XGBoost)
Perform feature importance analysis
Apply resampling techniques (SMOTE)
Hyperparameter tuning

Author
Esra Güneş
Computer Engineering Student
