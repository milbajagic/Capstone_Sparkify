# Project: Customer Churn Prediction 

This project was completed as part of the course requirements of [Udacity's](https://www.udacity.com/) Data Scientist Nanodegree certification.

## Project Overview
In this project, I used the machine learning APIs within Spark ML to build models to predict churn users for Sparkify, a fictional 
music streaming service.  

## Problem Statement 
Churn users are tricky to identify, but upon exploratory data analysis, I defined a churn user as a user who has 
submitted download and/or cancelled confirmation. I built a pyspark model locally, which can then be scaled on a full dataset on a 
distributed spark cluster. 

## Metrics 
Since only a small part of the dataset is defined as "churn", this caused a class imbalance. Due to this, we have to consider f1 score and recall. 
The recall shows how many of the churn users have actually been recognized by the model. To avoid identifying too many users as churn users, 
f1 score provides a mean of precision and recall. 

## Summary of results
Upon exploratory data analysis, and cleaning of data, following features were considered for model building: 
auth, gender, level, location, method, status, userAgent, hour and churn. To prepare data for modeling, categorical features were 
transformed using StringIndexer combined with OneHotEncoding. Upon testing LogisticRegression and RandomForestClassifier, it is hard to tell which model is better. They both performed equality well. This may be due to the small size of the data set used and to class imbalance. Hyperparameter tuning on a larger dataset in the cloud is necessary before selecting a model for successfully predicting user churn.


### Libraries used
This project requires Python 3.x and the following libraries installed: 
pandas, numpy, pyspark, matplotlib, seaborn

### Included files
* Sparkify.ipynb: The jupyter notebook containing the exploratory data analysis, feature engineering and model development
* mini_sparkify_event_data.json.zip: a subset (128MB) of the full dataset (12GB) used to explore with Spark before deploying cluster on the cloud
* Discussion of the notebook is presented in this blog post

### Acknowledgements
Sparkify dataset has been provided by [Udacity](https://www.udacity.com/).
