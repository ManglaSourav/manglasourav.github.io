---
layout: post
title: "How to clean data (Preprocessing Task)!!"
date: 2018-10-01 11:38:20 +0300
description:  Cleaning and Preparing data for ML . # Add post description (optional)
img:  # Add image post (optional)
---

## Data Preprocessing

Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, raw data is not feasible for the analysis. For achieving better results from the applied model in machine learning projects the data has to be cleaned.
There are some data cleaning techniques:

### 1 Each value should map onto a unique term (for nominal scale)

for Example,a variable Company may include a number of different spellings for the same company such as “General Electric Company,” “General Elec. Co.,” “GE,” “Gen. Electric Company,” “General electric company,” and “G.E. Company.” When these values refer to the same company, the various terms should be consolidated into one.

### 2 Numeric variables have some non-numeric terms

for example, a variable generally consisting of numbers may include a value such as “above 50” or “out of range.” Numeric analysis cannot interpret a non-numeric value and hence, these terms should be converted to a number or the observation removed.

### 3 Variables have some missing data values

Missing values are replaced or filled based on the type of data.  
**for discreate variable :** use mode or median value to fill the missing values.  
**for continuous variable :** use mean value to fill the missing values.

### 4 Removing outlier (for continuous variable)

Outliers are a single or a small number of data values that differ greatly from the rest of the values. We have to remove outliers.

### 5 Variables standardized to a single scale

A particular variable may have been measured over different units.
For example, a variable Weight may have been measured using both pounds and kilograms for different observations or a variable Price may be measured in different currencies. These should be standardized to a single scale so that they can be compared during analysis.
