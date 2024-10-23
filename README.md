## Credit Card Fraud Detection with Ensemble Learning

This project focuses on building a robust machine learning model for credit card fraud detection using ensemble methods. The main goal is to address the challenge of highly imbalanced datasets commonly found in fraud detection scenarios and achieve high accuracy while minimizing false positives.

**Datasets:**  
Dataset 1 : https://www.kaggle.com/datasets/prasy46/credit-card-fraud-detection/data  
Dataset 2 : https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data

**Key Features:**

* **Data Preprocessing:** The project starts with essential data preprocessing steps:
    * Checking data adequacy: Verifying the number of records and features for analysis.
    * Ensuring data quality: Using `df.info()` to understand data types, columns, and identify missing values.
    * Addressing missing values: Replacing null values with the mean of respective columns to ensure compatibility with algorithms like KNN.
    * Visualizing distribution patterns: Using histograms to gain insights into data distribution and identify potential trends or anomalies.
* **Handling Data Imbalance:**  Two techniques are employed to tackle the class imbalance problem:
    * Oversampling with SMOTE (Synthetic Minority Over-sampling Technique): This technique generates synthetic samples of the minority (fraudulent) class to balance the dataset.
    * Undersampling: This technique reduces the number of instances in the majority (non-fraudulent) class.
* **Model Training:** Three individual classifiers are trained and evaluated:
    * Random Forest Classifier
    * KNN (K-Nearest Neighbors) Classifier
    * XGBoost Classifier
* **Ensemble Methods:**  To enhance prediction accuracy and robustness, the project utilizes two ensemble methods:
    * Hard Voting:  The final prediction is based on the majority vote among the individual classifiers.
    * Soft Voting: The final prediction is based on the average of probabilities predicted by each classifier.
* **Evaluation Metrics:** The models are evaluated using various metrics:
    * Accuracy
    * Precision
    * Recall
    * F1-Score
    * ROC AUC (Receiver Operating Characteristic Area Under the Curve)
* **Comprehensive Analysis:** The project conducts a thorough comparison of model performance across different train-test splits (80:20, 70:30, and 60:40) and under both oversampling and undersampling approaches.

**Key Findings:**

* Oversampling using SMOTE significantly improves performance, particularly recall, compared to undersampling. 
* Ensemble methods, especially Hard Voting, consistently outperform individual classifiers, showcasing enhanced robustness in detecting fraudulent transactions.
* The models achieved high accuracy, precision, recall, and F1-score after oversampling and ensembling, indicating successful fraud detection capabilities.
* High ROC AUC scores demonstrate the models' robust ability to distinguish between fraudulent and non-fraudulent transactions.

**Conclusion:**

This project successfully demonstrates a comprehensive approach to credit card fraud detection by addressing data imbalance, leveraging ensemble learning, and evaluating various machine learning models. The best combination for this specific problem appears to be using oversampling with the Hard Voting ensemble method, achieving high performance across different evaluation metrics.
