# Kidney Disease Prediction - Predict whether the patient has kidney disease (1) or not (0)
The data set details are here - https://archive.ics.uci.edu/ml/datasets/chronic_kidney_disease

## Steps done to predict
1. Data pre-processing - Clean up missing values, null values etc. for numeric and categorical variables
2. Visualize the data to gain insights- Use heatmap to understand +ve/-ve correlations to target variable/ Use pair plot and box plot to study data and relations
3. Use scikit learn train_test_split to split the data to training and testing
4. Use XGBoost and cross validation to estimate the expected performance of the model
5. Use RandomizedSearchCV to get the best hyperparameters for XGBoost
6. Use Pipeline and pass StandardScaler and XGBClassifier as inputs
7. Train the model using XGBoost DMatrix and passing the best/optimal hyper parameters
8. Visualize the tree using plot_tree() function. This will tell us how the data is split across the trees
9. Visualize the important features used in the model using feature_importance() function
10. Do prediction
11. Validate the predictions by checking data and also using performance metrics such a accuracy, AUC and confusion matrix
12. Lastly checked with couple of other models such as DecisionTree and RandomForest to compare accuracy with XGBoost
