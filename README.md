# LifeExpectancy_Analysis
Machine Learning Model and Analysis of a dataset from WHO to better understand which variables have a significant in a countries' life expectancy.<br>

## Dataset
The dataset was obtained in the site Kaggle, via the following link: https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who.<br>
This dataset consists of data from the WHO (World Health Organization) about 22 variables related to 193 countries, collected between the years of 2000 and 2015.

## Premises
1. Dataset is correct: since I wasn't the one to collect the data, I'm assuming the creator of the dataset in Kaggle did it correctly. Also, even thought the WHO is a respected organization, we can't guarantee that all the data reflects perfectly the reality of the countries.<br>
2. Data reflects the present: as mentioned previously, this dataset consists of data from 2000 to 2015. In this study, we consider only the most recent year of each country. However, that still means that this data is from at most 2015, so it's possible that some of the variables changed drastically during this period.

## Method
### Data Treatment
A very classical approach was done for data treatment. First, all rows that contained null values were removed. Then, only data from the most recent year of collection for each country was considered (for example, if a country A doesn't have data from 2015 but has for 2014, it was considered data from 2014). The variable "Status" was also changed from a qualitative variable to a quantitative one. Finally, the country's name and year were removed, since they weren't important for the model.
### Model
For this study, it was used the Linear Regression Model. The choice was for its simplicity, but also for its accuracy for situations were the data is approximately linearily correlated (which is the case).<br>
To measure the accuracy of the model, it was used the metrics R2 and RSE, and also p_value analysis. Since we have 133 observations (a lot more than 30), the Student's t Distribution was replaced by the Normal Distribution.<br>
For the testing set, it was used the K-Fold method.
