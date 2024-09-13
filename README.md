# Ad Click Prediction using Machine Learning

## Project Overview

This project focuses on predicting whether a user will click on an advertisement based on various features such as time of day, age group, ad category, and its position on the webpage. The predictions were made using two different datasets:
1. **Imputed Dataset**: Missing values were handled using the KNN Imputer.
2. **Raw Dataset**: No imputation was applied, leaving the original null values.

## Data

The dataset contains the following key features:
- **Time of Day**: Morning, Afternoon, Evening, Night
- **Age Group**: 18-29, 30-39, 40-49, 50+
- **Ad Category**: Entertainment, Shopping, News, Technology, Sports
- **Ad Position**: Top, Bottom, Side
- **Click Status**: Whether a user clicked on the ad (1 = Yes, 0 = No)

## Project Workflow

1. **Data Preprocessing**:
   - **Scenario 1**: Missing values were imputed using the KNN Imputer.
   - **Scenario 2**: No imputation, the raw dataset with missing values was used.
   
2. **Modeling**:
   - Multiple Machine Learning algorithms were applied, including:
     - Random Forest
     - Histogram-based Gradient Boosting
     
   - **Hyperparameter tuning** was performed for both scenarios to optimize the models.

3. **Evaluation Metrics**:
   - Accuracy
   - Precision
   - Recall
   - F1-Score

## Results and Conclusion

### The Story the Data Tells for Successful Clicks:
- More ads should be scheduled in the **Afternoon** and **Morning**.
- Advertisers should target age groups of **20-29** and **30-39** for higher click rates.
- Ads in the categories of **Entertainment** and **Shopping** show higher success rates.
- Ads placed at the **Bottom** of the webpage have better results.

### Model Performance:
Two scenarios were evaluated:
1. **Imputed Dataset (KNN Imputer)**: Models were trained on the dataset with missing values imputed.
2. **Original Dataset (With Null Values)**: Models were trained on the dataset with null values.

After hyperparameter tuning, the **Random Forest** model performed slightly better than the **Histogram-based Gradient Boosting** in the second scenario (raw dataset with null values).

## Conclusion on ML Algorithms:
- The **Random Forest** model outperformed **Histogram-based Gradient Boosting** in the second scenario (raw dataset with null values), making it a better choice for deployment in this context.
  
## Requirements

- Python 3.x
- Scikit-learn
- Pandas
- NumPy
- KNNImputer

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ad-click-prediction.git

