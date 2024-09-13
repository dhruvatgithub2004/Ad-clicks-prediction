# Ad Click Prediction using Machine Learning

## Project Overview

This project focuses on predicting whether a user will click on an advertisement based on various features such as time of day, age group, ad category, and its position on the webpage. The predictions were made using two different datasets:
1. **Imputed Dataset**: Missing values were handled using the KNN Imputer.
2. **Raw Dataset**: No imputation was applied, leaving the original null values.

## Data

The dataset contains the following key features:
- **Age**
- **Gender**
- **Device Type**
- **Ad Position**: Top, Bottom, Side
- **Browsing History**: Past activity on the website
- **Time of Day**: Morning, Afternoon, Evening, Night
- **Click Status**: Whether a user clicked on the ad (1 = Yes, 0 = No)

## Project Workflow

1. **Data Preprocessing**:
   - **Scenario 1**: Missing values were imputed using the KNN Imputer.
   - **Scenario 2**: No imputation, the raw dataset with missing values was used.
   
2. **Modeling**:
   - **Scenario 1 (Imputed Dataset)**:
     - Models used: 
       - Logistic Regression (LR)
       - Random Forest (RF)
       - KNeighborsClassifier (KNC)
       - Support Vector Classifier (SVC)
       - Voting Classifier (combining multiple models)
   
   - **Scenario 2 (Raw Dataset with Null Values)**:
     - Models used:
       - Random Forest (RF)
       - Histogram-based Gradient Boosting (HGB)
     
   - **Hyperparameter tuning** was performed for all models in both scenarios to optimize performance.

3. **Evaluation Metrics**:
   - F1 Score
   - Confusion Matrix
   - Accuracy
   - Classification Report

## Results and Conclusion

### The Story the Data Tells for Successful Clicks:
- More ads should be scheduled in the **Afternoon** and **Morning**.
- Advertisers should target age groups of **20-29** and **30-39** for higher click rates.
- Ads in the categories of **Entertainment** and **Shopping** show higher success rates.
- Ads placed at the **Bottom** of the webpage have better results.

### Model Performance:
Two scenarios were evaluated:
1. **Imputed Dataset (KNN Imputer)**: Models trained on the imputed dataset included Logistic Regression, Random Forest, KNeighborsClassifier, SVC, and a Voting Classifier.
2. **Original Dataset (With Null Values)**: Models trained on the raw dataset with null values were Random Forest and Histogram-based Gradient Boosting.

After hyperparameter tuning, the **Random Forest** model outperformed **Histogram-based Gradient Boosting** in the second scenario (raw dataset with null values).

## Conclusion on ML Algorithms:
- In the second scenario (raw dataset with null values), the **Random Forest** model slightly outperformed **Histogram-based Gradient Boosting**, making it a better choice for deployment.

## Requirements

- Python 3.x
- Scikit-learn
- Pandas
- NumPy
- KNNImputer
