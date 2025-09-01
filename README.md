# 🔄 Customer Churn Prediction

## 📌 Project Overview
This project focuses on **predicting customer churn** using machine learning techniques and feature engineering.

- 🔍 **Comprehensive Data Exploration** – analyzing customer demographics, usage patterns, and relationships with churn
- 🛠 **Feature Engineering** – creating time-based features, encoding categorical variables, and applying transformations
- 📊 **Data Transformation** – applying log transformation to handle skewed features
- 🤖 **Predictive Modeling** – comparing Logistic Regression and Random Forest models
- 🎯 **Goal** – identify key churn factors and build an accurate prediction model for customer retention strategies

## Dataset
The dataset contains information about customers, with the following features:

- **Age**: Customer age in years
- **Gender**: Customer gender
- **Tenure**: Length of time as a customer (in months)
- **Usage Frequency**: How often the customer uses the service
- **Support Calls**: Number of support calls made by the customer
- **Payment Delay**: Average days of payment delay
- **Total Spend**: Total amount spent by the customer
- **Last Interaction**: Days since the last interaction
- **Subscription Type**: Type of subscription (Basic or Premium)
- **Contract Length**: Duration of the contract (Monthly, Quarterly, or Annual)
- **Churn**: Whether the customer has churned (0 = No, 1 = Yes) - target variable

---

## Key Techniques Implemented

- **Data Exploration & Visualization**
  - Missing value analysis
  - Statistical summary of features
  - Correlation analysis between numerical features
  - Distribution analysis of categorical variables
  - Churn rates by contract length and subscription type
  - Visualization of churn patterns across different customer segments

- **Feature Engineering & Data Preprocessing**
  - Label encoding of categorical features
  - Creation of time-based derived features:
    - Tenure-to-Age ratio
    - Monthly spend calculation
    - Relative inactivity
    - Support calls per month
    - Usage frequency per month
  - Log transformation of skewed features
  - Feature scaling with `StandardScaler`

- **Model Training & Evaluation**
  - Logistic Regression classifier
  - Random Forest classifier
  - Performance metrics:
    - Accuracy, precision, recall, and F1-score
    - Detailed classification reports
  - Comparison of model performance across metrics

- **Visualization of Results**
  - Churn distribution analysis
  - Effect of categorical features on churn
  - Correlation matrix heatmap
  - Before/after transformation visualizations

---

## Results
The models achieved the following performance metrics:

### Logistic Regression:
- Accuracy: 0.5698
- Precision: 0.5242
- Recall: 0.9934
- F1 Score: 0.6863

### Random Forest:
- Accuracy: 0.5036
- Precision: 0.4883
- Recall: 0.9985
- F1 Score: 0.6558

Key findings include:
- Both models show extremely high recall but moderate precision
- Contract Length was a significant predictor of churn, with monthly contracts showing higher churn rates
- Support Calls and Tenure showed meaningful correlation with churn
- The models excel at identifying customers who will churn but generate many false positives
- Logistic Regression slightly outperformed Random Forest in overall metrics

---

## Requirements
- Python 3
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

## How to Use
1. Clone this repository
2. Ensure you have all required packages installed
3. Open the Jupyter notebook `Customer_Churn_Prediction_Condensed.ipynb`
4. Run the cells sequentially to see the analysis and results

---

## File Structure
- `Customer_Churn_Prediction.ipynb` - The main Jupyter notebook containing all analysis and code
- `customer_churn_dataset-training-master.csv` - Training dataset with churn information
- `customer_churn_dataset-testing-master.csv` - Testing dataset for evaluation
- `README.md` - This file with project information

---

## Key Insights
- Feature engineering (especially time-based features) provides valuable signals for churn prediction
- Log transformation effectively addresses the skewness in certain features
- Both models show a strong bias toward predicting churn, leading to high recall but moderate precision
- The current models would be most useful in scenarios where the cost of missing a potential churner is high
- There's potential for improvement by addressing class imbalance and further feature engineering
- Contract length and support call frequency are key indicators of potential churn
