# Depression project overview
Created a tool that predicts whether one's stress level is healthy or not. Excessive stress might lead to depression.

## Code and Resources Used
**Python Version:** `3.8.6`

**Packages:** `pandas, numpy, matplotlib, seaborn, sklearn, imblearn`

## Data Cleaning
After loading the data, I needed to clean it up so that it was usable for our model. I made the following changes:
* removed redundant features/rows,
* checked for any null values,
* ckecked if all of the features are of the correct type (numeric)

## EDA
I created a countplot to realize that more than twice as many people in our dataset didn't experience unhealthy stress compared to those who did.
Out of those who did experience unhealthy stress more females than males are exposed to excessive stress. I also created new feature - our target('UNHEALTHY_STRESS') 
based on existing one (DAILY_STRESS) and dropped the latter.

## Model Building
First, I handled categorical features - transformed the categorical variables into dummy variables. I then scaled numerical features for better performance using StandardScaler. After that I balanced the data using SMOTE. I also split the data into train and test subsets with a test size of 20%. After that, I performed a feature selection using:
Variance Threshold, Pearson Correlation and Information Gain.

I built a Logistic Regression Model using 10 best features.

## Model performance
After doing analysis of weights it is clear that in order to prevent high stress level leading to depression it is necessary to maintain sufficient income, have enough time spent on daily meditation (or praying) and get the correct amount of sleep. Factors such as daily shouting or lost vacation contribute to higher stress level.
