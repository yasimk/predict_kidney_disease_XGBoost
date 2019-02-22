# Kidney Disease Prediction - Predict whether the patient has kidney disease (1) or not (0)
The data set details are here - https://archive.ics.uci.edu/ml/datasets/chronic_kidney_disease

## Objective of this model - Predict whether a patient will have kidney disease or not based on historical data. 
1) Identify the top factors that contribute to kidney disease prediction
2) Measure the accuracy of the model
3) Do prediction

I have used XGBoost algorithm here for prediction. Extreme Gradient boosting (XGBoost) is a supervised learning algorithm that attempts to predict a target variable by combining the estimates of a set of simpler, weaker models. XGBoost has done remarkably well in machine learning competitions because it robustly handles a wide variety of data types, relationships, and distributions. It often is a useful, go-to algorithm in working with structured data, such as data that might be found in relational databases and flat files.

## Steps done to do the prediction using XGBoost

### 1. Data pre-processing - Clean up missing values, null values etc. for numeric and categorical variables
![kidney_prediction_missingvalues-01](https://user-images.githubusercontent.com/34105353/51875882-5e59fe00-232c-11e9-92a2-7b7f69829356.png)

### 2. Visualize the data to gain insights- Use heatmap to understand +ve/-ve correlations to target variable
![kidney_prediction_heatmap](https://user-images.githubusercontent.com/34105353/51875881-5e59fe00-232c-11e9-9a8f-a3d3b6b8be5e.png)

### Use pair plot to study data and gain insights
![kidney_prediction_pairplot-01](https://user-images.githubusercontent.com/34105353/51875878-5dc16780-232c-11e9-8311-23f6130ee441.png)

### Use box plot to study data and gain insights
![kidney_prediction_boxplot-01](https://user-images.githubusercontent.com/34105353/51876161-3e770a00-232d-11e9-90ea-4ce79f5621ba.png)

### 3. Use scikit learn train_test_split to split the data to training and testing

### 4. Use XGBoost and cross validation to estimate the expected performance of the model
![kidney_prediction_model_auc_performance](https://user-images.githubusercontent.com/34105353/51875883-5e59fe00-232c-11e9-85b9-b88295d5db4c.png)

### 5. Use RandomizedSearchCV to get the best hyperparameters for XGBoost

### 6. Use Pipeline and pass StandardScaler and XGBClassifier as inputs

### 7. Train the model using XGBoost DMatrix and passing the best/optimal hyper parameters

### 8. Visualize the tree using plot_tree() function. This will tell us how the data is split across the trees
![xgb plot tree](https://user-images.githubusercontent.com/34105353/51875879-5dc16780-232c-11e9-94ab-0024b76fbe4c.png)

### 9. Visualize the important features used in the model using feature_importance() function
![xgboost_kidney_disease_feature_importance](https://user-images.githubusercontent.com/34105353/51875880-5e59fe00-232c-11e9-8922-f35237944ac6.png)

### 10. Do prediction

### 11. Validate the predictions by checking data and also using performance metrics such a accuracy, AUC and confusion matrix

### 12. Lastly checked with couple of other models such as DecisionTree and RandomForest to compare accuracy with XGBoost

