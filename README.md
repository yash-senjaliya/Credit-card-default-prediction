### Credit-card-default-prediction


1. To perform modeling on the dataset, 80% of the data is training and to check how the model is performing 20% of the data is test.
2. After having the analysis and visualization of the independent variables/features, there are few major noticeable outliers which needs to be removed to avoid fitting issues.

    2.1 Features having the count of behind due date in the emi repayment have a common pattern of outliers which are clipped.
    
    2.2 Removing the rows where data entry errors are noticeable in case of Debt Ratio and removal of rows which do not make any sense as per the description of some feature.

3. Missing value is imputed using the mean and mode as per the type of the feature.

4. Features are engineered to make a model more robust and more informative in decision making to better classify non delinquent borrowers to delinquent borrowers. For that interaction of the features are performed and binary indicators to capture yes/no behaviour.

5. To tackle class imbalance issue upsampling and synthetic samping of the minority clas along with the downsampling of the majority class is done to better train a model.

6. Feature Scaling is done so that certain models such as Neural Network and Logistic Regression which relies on features weights to minimise error.

7. For tree based models, no feature scaling is done as performance with or without feature scaling is nearly same.

8. Training of the models using NN, LR, Tree Based Models are done with few techniques to compare results which are feature scaling, tackling class imbalance issue with synthetic sampling and assigning class weights itself in the model using their hyperparameter.

9. For tree based models, hyperparameters were tuned using GridSearchCV to  have the optimal solution.

10. After doing all the kinds of modeling, it was found that Logistic Regression and NN performs when scaling of the features are done if a scale or range of features are very different from each other.  

11. Tree based models were performing the best and among them LightGBM performance was better after looking at the feature importance and other metrics. Hence, LightGBM was chosen to train the model and predict the unseen data.

12. Metrics were chosen apart from Accuracy to accurately check how the model was performing. 

13. How the model was behaving internally at a global level was checked using SHAP and at a local level was checked using LIME.
