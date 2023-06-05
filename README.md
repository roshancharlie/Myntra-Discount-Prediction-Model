# Myntra Discount Prediction Model Using Machine Learning

This repository contains a machine learning model for predicting discounts on fashion clothing items on Myntra. The project involves data cleaning, preprocessing, feature engineering, exploratory data analysis, and regression analysis. The model performance is improved by applying logarithmic scaling to the features.

## Table of Contents
- [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Regression Analysis](#regression-analysis)
- [Logarithmic Scaling](#logarithmic-scaling)
- [Results](#results)

## Data Cleaning and Preprocessing
In this step, the dataset is cleaned and preprocessed to handle missing values and convert data types. The "DiscountOffer" column is filled with 0 for missing values and converted to string data type. A new column called "DiscountOffer_len" is created to store the length of the strings in the "DiscountOffer" column. The data is then split into different groups based on the length of the strings, and the discount amount is segregated into separate columns for each group. The discounted price is calculated for each group and stored in a new column. Finally, all the groups are concatenated back into one dataframe.

## Feature Engineering
The feature engineering process involves creating new features and merging relevant information. The dataset is filtered to separate out instances where the discount percentage is zero. The filtered data is split into training, validation, and test sets. Average rating and total reviews are calculated for each brand, creating a new column called "Brand_importance." The importance values are merged back to the datasets. The number of unique brands in each category is calculated and stored in a column called "ind_cat_popularity," which is also merged back to the datasets. Additionally, the number of products in each category is calculated and stored in a column called "cat_popularity," which is merged back to the datasets.

## Exploratory Data Analysis (EDA)
EDA is performed on the "model_data" dataset using the Seaborn and Matplotlib libraries. A heatmap is created to visualize the correlation between different features. The correlation between the target variable and the features is plotted as a bar chart. A pairplot is also created to visualize the relationships between variables.

## Regression Analysis
Three regression models are used: Linear Regression, KNeighbors Regressor, and Random Forest Regressor. For each model, a model object is created, and it is fitted on the training data. The accuracy of the models is evaluated on the test and validation data using the r2_score function. The feature importance of the Random Forest Regressor model is also calculated and stored in a dataframe.

## Logarithmic Scaling
To improve the model performance, logarithmic scaling is applied to the features of the training, testing, and validation data. This transformation helps balance the magnitude of each feature and makes the data more normally distributed. Logarithm is applied to the feature values, and a small value is added to avoid taking the logarithm of zero.

## Results
The model performance improves after applying logarithmic scaling to the features. The accuracy of the Linear Regression model, KNeighbors Regressor model, and Random Forest Regressor model show improvement. Detailed results and analysis can be found in the project code.



<div align="center">
<h3> Connect with me<a href="https://gifyu.com/image/Zy2f"><img src="https://github.com/milaan9/milaan9/blob/main/Handshake.gif" width="60"></a>
</h3> 
<p align="center">
    <a href="mailto:roshanguptark432@gmail.com" target="_blank"><img alt="Gmail" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/Gmail.svg"></a> 
    <a href="https://www.linkedin.com/in/roshan-sinha/" target="_blank"><img alt="LinkedIn" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/Linkedin.svg"></a>
    <a href="https://www.instagram.com/roshan_the_constant/?hl=en" target="_blank"><img alt="Instagram" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/Instagram.svg"></a>
    <a href="https://www.hackerrank.com/roshanguptark432" target="_blank"><img alt="HackerRank" width="25px" src="https://github.com/TheDudeThatCode/TheDudeThatCode/blob/master/Assets/HackerRank.svg"></a>
    <a href="https://github.com/roshancharlie" target="_blank"><img src="https://cdn.svgporn.com/logos/github-icon.svg" alt="Github logo" width="25px"></a>
</p>  
