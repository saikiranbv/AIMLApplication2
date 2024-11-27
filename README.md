# AIMLApplication
# AIML Application for Regression

# The Notebook file path is 
 The data vehicles.csv is in data folder

# The business objective is to identify the key factors influencing used car prices.

# To acheive this, We will build a predictive model where the target variable is the price of a used car.
# The goal is to analyze the relationships between the car's price and various features given in the dataset.
# Using the Machine Learning techniques learnt so far, we need to Quantify the contribution of each feature to the car's price.
# Using the Machine Learning techniques learnt so far, we need to Quantify the contribution of each feature to the car's price.

# Here a the final conculsions 
# 1. The Age of the car and Odometer Reading have the maximum influence. Both imact the price negatively 
# 2. Cylinders, Transmission and model have some influence on the price
# 3. The Ridge regression model with polynomial degree = 4 and alpha = 1 is the best fit for predicting the Used car sale price

# Here are the details....


# This will require the following tasks 
# Data preparation i.e. removing outliers, handling missing values and encoding
# Exploratory data analysis thru different visializations of the data and relationships
# Regression modeling to extract meaningful insights and make reliable predictions

# Observation-1: The dataset has 4 numerical features and 14 categorical features

# Observation-2: There are quitea few null values. Size has 71% null values, Condition and Cylinders have over 40%

# Observation-3: Based on the summary statistics and unique values, here are few more observations
# 1. There are few columns that don't directly contribute to the calculation of price e.g. Id, VIN
# 2. Some of the numeric data has outliers that is seen from Max value as well as Standard Deveiation. Need to clean the outliers
# 3. There are quite a few missing values. Need to remove columns, remove rows with missing values and imputation (replaces missing data)e.g. size
# 4. We have 'year' as input but 'age' of car is of business value. So need to convert year to age of the car

# Observation-4: Now the data has no outliers as seen in the statistics. We need to do more deeper visual analysis

# Observation-5: The Price data is right skewed distribution 

# Observation-6: The manufacturers Ford, Chevy followed by Toyota and Honda sell the most cars 

# Observation-7: 6 & 8 cylinders are most popular
# Price goes down as Odometer reading goes up 
# As Age goes up, average price goes down..

# Observation-8: The Region data is too extensive for any meaningful insights. Same with Model data
# Ferrari cars have higher price than other cars
# Looig at the 2-D graphs, there are no more outliers that we need to deal with except for missing data.. 

# Observation-9: The Aga and Odometer are negatively related to and impact the price of the car
# The number of cylinders has only minor impact

# Observation-10: Now we have filled all the missing data, Build the correlation heatmap between the numberical value features 

# Observation-11: Clearly age and odometer have impact on price. The rest of them have only minimal impact

# Modeling, we shall try the following 3 methods on each dataset and verify the results 
# Linear Regression
# Ridge Regression
# Lasso Regression 

# Observation on Linear Regression Models - The set 3 has better Train and Test MSE values as well as R2 scores

# Based on trial and error we got {'polyfeatures__degree': 3, 'ridge__alpha': 1}  we shall use this for calculation

# Observation on Ridge Regression Models - The set 3 has better Train and Test MSE values as well as R2 scores
# Also the best hyperparameters are ploomial dgree and alpha of 1
