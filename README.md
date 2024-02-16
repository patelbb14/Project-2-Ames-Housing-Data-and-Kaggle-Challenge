# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Data and Kaggle Challenge

### Overview

Welcome to Project 2! It's time to start modeling.

**Primary Learning Objectives:**

1. Creating and iteratively refining a regression model
1. Using [Kaggle](https://www.kaggle.com/) to practice the modeling process
1. Providing business insights through reporting and presentation.

You are tasked with creating a regression model based on the Ames Housing Dataset. This model will predict the price of a house at sale.

The Ames Housing Dataset is an exceptionally detailed and robust dataset with over 70 columns of different features relating to houses.

Secondly, we are hosting a competition on Kaggle to give you the opportunity to practice the following skills:

- Refining models over time
- Use of train-test split, cross-validation, and data with unknown values for the target to simulate the modeling process
- The use of Kaggle as a place to practice data science

As always, you will be submitting a technical report and a presentation. **You may find that the best model for Kaggle is not the best model to address your data science problem.**


### Problem Statement

You work for a real estate company. Your higher ups have asked you to identify the best predictors of house sale prices. Your company wants to know what gives potential customers a reliable estimate of the value of the property that is on sale or will be on sale and to ultimately increase revenue. Using the training and test datasets that are provided, use different regression methods such as linear, ridge and lasso to make your models and see which one makes the best predictions. 

---

### Datasets

#### Provided Data

There are 3 datasets included in the [`datasets`](./datasets/) folder for this project. We have train.csv, test.csv, and sample_sub_reg.csv. We will be using the train.csv and test.csv for our models. No outside datasets will be used as we are doing train/test predictions.

#### Data Dictionary
From the documentation below, we learn that there are 2930 observations and 82 variables. Additionally, the data has 82 columns which include 23 nominal, 23 ordinal, 14 discrete, and 20 continuous variables (and 2 additional observation identifiers).

Please see the link below for the original data dictionary:
https://jse.amstat.org/v19n3/decock/DataDocumentation.txt

---

### Executive Summary


You work for a real estate company. Your higher ups have asked you to identify the best predictors of house sale prices. Your company wants to know what gives potential customers a reliable estimate of the value of the property that is on sale or will be on sale. The objective of this project is to use the training and test datasets that are provided, and use different regression methods such as linear, ridge and lasso to make your models and see which one makes the best predictions. 

Data sources that were used in the project were provided. There were two datasets (train.csv and test.csv). The methodology of the project is as follows :
- After reading in train.csv and test.csv, data exploratory was done to see what features would be the best fit to use in the model
- Next, data cleaning was done to ensure there were no NAs, the data types were correct, if category columns were used made sure they were OneHotEncoded, and made sure that both train and test datasets had the same columns
- Then, ran different models for 6 different runs using linear regression, ridge regression, and lasso regression
- Finally, evaluated the models by looking at the R-squared values and RMSE.

As part of the project, we needed to do Kaggle submissions. Once the models were finished, outputs were created, which were then submitted to Kaggle.

Based on all of the models run, the best model was the Top 15 correlated numeric variables using RidgeCV. However, if we look at the Kaggle submissions, the best model was the Top 15 correlated numeric variables with LassoCV. The R-squared and RMSE for the model I ran using RidgeCV were 0.77 and 25085. The R-squared and RMSE for the model I ran using LassoCV were 0.77 and 27809 (not Kaggle).

Next steps for this project would be to bring in categorical variables and seeing how numeric and categorical variables together would impact the models. Also, looking into changing the alphas in the RidgeCV and LassoCV would be another choice.
