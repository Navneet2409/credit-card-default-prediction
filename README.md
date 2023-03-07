# credit-card-default-prediction
The goal of credit card default prediction is to help credit card companies and lenders to better manage their risk and minimize losses. Overall, credit card default prediction is an important tool for lenders to manage risk and ensure the stability of the credit card industry.

## Table of Content
  * [Problem Statement](#problem-statement)
  * [Dataset](#dataset)
  * [Data Pipeline](#data-pipeline)
  * [Project Structure](#project-structure)
  * [Conclusion](#conclusion)


## Problem Statement
A credit card issuer based in Taiwan wants to learn more about how likely its customers are to default on their payments and the main factors that influence this probability. The issuer's decisions regarding who to issue a credit card to and what credit limit to offer would be informed by this information. The issuer's future strategy, including plans to offer targeted credit products to their customers, would be informed by a better understanding of their current and potential customers as a result of this.


## Dataset
This dataset contains information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005. For more information on the dataset, please visit the Kaggle website at https://www.kaggle.com/code/selener/prediction-of-credit-card-default/input


## Data Pipeline
  1. Analyze Data: 
      In this initial step, we attempted to comprehend the data and searched for various available features. We looked for things like the shape of the data, the 
      data types of each feature, a statistical summary, etc. at this stage.
  2. EDA: 
      EDA stands for Exploratory Data Analysis. It is a process of analyzing and understanding the data. The goal of EDA is to gain insights into the data, identify 
      patterns, and discover relationships and trends. It helps to identify outliers, missing values, and any other issues that may affect the analysis and modeling 
      of the data.
  3. Data Cleaning: 
      Data cleaning is the process of identifying and correcting or removing inaccuracies, inconsistencies, and missing values in a dataset. We inspected the dataset 
      for duplicate values. The null value and outlier detection and treatment followed. For the imputation of the null value we used the Mean, Median, and Mode 
      techniques, and for the outliers, we used the Clipping method to handle the outliers without any loss to the data.
  4. Feature Selection: 
      At this step, we did the encoding of categorical features. We used the correlation coefficient, encoding, feature manipulation, and feature selection techniques to select 
      the most relevant features. SMOTE is used to address the class imbalance in the target variable.
  5. Model Training and Implementation:  
      We scaled the features to bring down all of the values to a similar range. We pass the features to 8 different classification models. We also did 
      hyperparameter tuning using GridSearchCV.
  6. Performance Evaluation: 
      After passing it to various classification models and calculating the metrics, we choose a final model that can make better predictions. We evaluated different 
      performance metrics but choose our final model using the f1 score and recall score.


## Project Structure
```
├── README.md
├── Dataset 
│   ├── 
├── Problem Statement
│
├── Know Your Data
│
├── Understanding Your Variables
│
├── EDA
│   ├── Numeric & Categorical features
│   ├── Univariate Analysis
│   ├── Bivariate and Multivariate Analysis
│
├── Data Cleaning
│   ├── Duplicated values
│   ├── Missing values
│   ├── Skewness
│   ├── Treating Outliers
│ 
├── Hypothesis Testing
│
├── Feature Engineering
│   ├── Feature Manipulation
|   ├── Encoding
|   ├── Correlation Coefficient and Heatmap
│   ├── Feature Selection
|   ├── Smote
│
├── Model Building
│   ├── Train Test Split
|   ├── Scaling Data
|   ├── Model Training
│
├── Model Implementation
│   ├── Logistic Regression
|   ├── KNN
│   ├── Decision Tree
|   ├── Random Forest
|   ├── AdaBoost
│   ├── XGBoost
|   ├── LightGBM
|
├── Model Result and Implementation
|   ├── Model Result
|   ├── Model explainability
|   ├── Conclusion
|
| 
└── Reference
```


## Conclusion
In this project, we tackled a classification problem in which we had to classify and predict whether a credit card holder is likely to default on their payments. This problem is important for credit card companies, as it allows them to identify risky borrowers and take appropriate measures to minimize their losses.
    - There were 30000 records and 25 attributes in the dataset.
    - We started by importing the dataset, and necessary libraries and conducted exploratory data analysis (EDA) to get a clear insight into each feature by separating the 
      dataset into numeric and categoric features. We did Univariate, Bivariate, and even multivariate analyses.
    - After that, the outliers and null values were checked from the raw data. Data were transformed to ensure that it was compatible with machine learning models.
    - In feature engineering, we transformed raw data into a more useful and informative form, by encoding, feature manipulation, and feature selection. We handled 
      target class imbalance using SMOTE.
    - Then finally cleaned and scaled data was sent to various models, the metrics were made to evaluate the model, and we tuned the hyperparameters to make sure the right 
      parameters were being passed to the model. To select the final model based on requirements, we checked model_result.
    - When developing a machine learning model, it is generally recommended to track multiple metrics because each one highlights distinct aspects of model performance. We are, 
      however, focusing more on the Recall score and F1 score because we are dealing with credit card data and our data is unbalanced.
    - Our highest recall score, 0.908, came from KNN.
    - The LightGBM, XGBoost, and RandomForestClassifier also provided the best approach to achieving our goal. We were successful in achieving a respective f1-score of 0.866, 0.867, and 0.868.

The recall score is of the utmost significance in the banking field, where we place a greater emphasis on reducing false negative values because we do not want to mispredict a person's default status when he has defaulted. With recall scores of 0.908, 0.827, and 0.815, respectively, KNN, RandomForest, and XGB performed the best.

    - Last but not least, we can select the Final model as our KNN classifier due to its highest recall score.



