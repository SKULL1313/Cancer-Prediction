# Breast-Cancer-Classification

## End of Project Report: Logistic Regression on Breast Cancer Data

### 1. Title and Introduction

**Title**: Logistic Regression Analysis for Breast Cancer Classification

**Introduction**:  
The objective of this project was to develop a logistic regression model that can classify breast cancer tumors as malignant or benign based on various features of cell nuclei present in a digitized image of a fine needle aspirate (FNA) of a breast mass. The goal was to build a predictive model that assists in the early detection and diagnosis of breast cancer, which is critical for effective treatment and management.

### 2. Data Overview

The dataset used in this analysis is the Breast Cancer Wisconsin (Diagnostic) dataset, which consists of 569 observations of breast cancer cases. Each observation includes 30 features that describe characteristics of cell nuclei, such as radius, texture, perimeter, area, smoothness, compactness, and more.

**Key features include:**

- **Radius (mean)**: Mean of distances from the center to points on the perimeter.
- **Texture (mean)**: Standard deviation of gray-scale values.
- **Perimeter (mean)**: Perimeter of the tumor.
- **Area (mean)**: Area of the tumor.
- **Smoothness (mean)**: Local variation in radius lengths.

The target variable is the diagnosis, which indicates whether the tumor is malignant (M) or benign (B).

### 3. Data Cleaning and Preparation

Before training the model, data cleaning and preprocessing steps were carried out:

- **Missing Values**: A heatmap was used to visualize missing values, revealing that certain columns contained null values. These columns, along with an unnamed ID column, were dropped from the dataset.
- **Encoding**: The diagnosis column, which originally contained categorical values ('M' for malignant and 'B' for benign), was encoded into numerical values (1 for malignant and 0 for benign).
- **Normalization**: To ensure that all features are on the same scale, the data was normalized using the StandardScaler. This step is crucial for logistic regression as it improves the model's convergence and accuracy.

### 4. Modeling

The logistic regression model was chosen due to its effectiveness in binary classification tasks. The data was split into training and testing sets, with 70% of the data used for training and 30% for testing.

**Training**:  
The model was trained on the scaled training data, and then predictions were made on the test data.

**Model Performance**:

- **Accuracy**: The model achieved an accuracy of 98%, indicating that it correctly classified the tumors in 98% of the cases.
- **Confusion Matrix**: The confusion matrix revealed that the model had a low number of false positives and false negatives.
- **Classification Report**: The report provided further insights into the precision, recall, and F1-score for both classes (malignant and benign).

### 5. Evaluation

The logistic regression model was evaluated using various metrics:

- **Accuracy**: The model's accuracy was 0.98, meaning it correctly identified 98% of the test cases.

**Confusion Matrix**:

- **True Positives (TP)**: The number of malignant cases correctly identified.
- **True Negatives (TN)**: The number of benign cases correctly identified.
- **False Positives (FP)**: Benign cases incorrectly classified as malignant.
- **False Negatives (FN)**: Malignant cases incorrectly classified as benign.

**Classification Report**:

- **Precision**: High precision indicates that the model correctly identified the majority of malignant cases.
- **Recall**: High recall suggests that the model was effective in identifying actual malignant cases.
- **F1-Score**: The F1-score balances precision and recall, confirming the model's robustness.

### 6. Conclusion

The logistic regression model proved to be a highly effective tool for classifying breast cancer tumors, with a strong accuracy rate and reliable performance metrics. This model could be valuable in assisting medical professionals with early and accurate diagnosis of breast cancer, ultimately contributing to better patient outcomes.

### Next Steps:

- **Model Improvement**: Explore other classification models like Support Vector Machines (SVM) or Random Forest to see if they offer better performance.
- **Feature Selection**: Conduct further analysis to identify the most significant features, potentially simplifying the model while maintaining accuracy.
- **Cross-Validation**: Perform cross-validation to ensure the model's stability and generalizability across different subsets of data.

This report highlights how logistic regression can be effectively applied to a critical healthcare problem, providing actionable insights and supporting decision-making in breast cancer diagnosis.
