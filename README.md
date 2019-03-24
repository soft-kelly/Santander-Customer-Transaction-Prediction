# Santander-Customer-Transaction-Prediction
This is from Kaggle Featured Prediction Competition. Here is the link: https://www.kaggle.com/c/santander-customer-transaction-prediction

In this challenge, Santander invites Kagglers to help them identify which customers will make a specific transaction in the future, irrespective of the amount of money transacted. The data provided for this competition has the same structure as the real data they have available to solve this problem. To protect the privacy, the given data doesn't have a real column name. All columnes name looks like ID_code, target, var_0, var_1 and so on.

To solve this problem, I did following four steps: clean the data, build up models, generate new features and select model. And you can find all the coding with Python/R in this repository.

## Clean the data 
There are 200,000 samples in the test dataset. For each sample, we have 200 features named from var_0 to var_199, one binary target, and one ID_code. There are no missing values in the dataset. So I only removed the columne ID_code. I noticed that the target is unbalanced, 10% is 1 and 90% is 0. Also, the correlation coefficient matrix told us the features are independent with each other.

## Build up Models 
I build up models by boosting algorithms: xgboost, lgbm and catboost. I chose the parameters by Bayesian Optimization. 
### xgboost

### lgbm

### Catboost

### Bayesian Optimization


I also tried other interesting approaches: time analysis with prophet and uber ludwig. I didn't post code for those two. But here are some introduction for people who are interest.

### time analysis
Some people said the var_68 is date and can be decoded to dates from 2017-07-24 to 2019-01-06 (https://www.kaggle.com/c/santander-customer-transaction-prediction/discussion/84450). From there, we can use FaceBook prophet to do time analysis(https://facebook.github.io/prophet/). But it didn't work out for me. 

### uber ludwig
Ludwig is a toolbox that allows to train and test deep learning models without the need to write code (https://uber.github.io/ludwig/). Since it got 0.75 accuracy in Kaggle's Titanic: Predicting survivors, I did not put too much time on this.

## Generate New Features 
Aim to multiply features. 

## Select Model
| Algorithm Name | Cross-Validation Score | Leaderboard Score| Running time |
| ------------- | ----------------------  |----------------- |------------- |
| XGBoost       | Content Cell            |Content Cell      |Content Cell  |
| CatBoost      | Content Cell            |Content Cell      |Content Cell  |
| LGBoost       |   Content Cell          |Content Cell      |Content Cell  |
