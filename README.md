# Myntra Discount Prediction Model Using Machine Learning

### I have perform data cleaning and preprocessing on a fashion clothing dataset from Myntra. The following steps are performed:

- Importing necessary libraries: pandas, numpy, matplotlib, seaborn, and opendatasets.
- Downloading the dataset using the opendatasets library.
- Filling missing values in the "DiscountOffer" column with 0 and converting the column to string data type.
- Creating a new column "DiscountOffer_len" that contains the length of the strings in the "DiscountOffer" column.
- Splitting the data into different groups based on the length of the "DiscountOffer" strings.
- Segregating the discount amount into a separate column "Discount_Seg" for each group.
- Calculating the discounted price for each group in a new column "discount_seg_price".
- Concatenating all the groups back into one dataframe.

### Then I have perform preprocessing on a data set containing information about products For Feature Engineering. The following steps are performed:

- Filter out the data where discount percentage is zero into a separate dataframe called "Non_Discount_data".
- Split the filtered data into training, validation, and test sets using the "train_test_split" function from the scikit-learn library.
- Calculate the average rating and total reviews for each brand and create a new column "Brand_importance".
- Merge the brand importance values back to the training, validation, and test data sets.
- Calculate the number of unique brands in each individual category and create a new column "ind_cat_popularity".
- Merge the individual category popularity values back to the training, validation, and test data sets.
- Calculate the number of products in each category and create a new column "cat_popularity".
- Merge the category popularity values back to the training, validation, and test data sets.
- Repeat steps 4-8 for the "Non_Discount_data" dataframe.

### Then I have Perform Exploratory Data Analysis (EDA) On "model_data". It uses the Seaborn and Matplotlib libraries in Python. The following steps are performed:

- A heatmap is created to show the correlation between different features in the X_train data.
- The correlation between the target variable (y_train) and the features in X_train is plotted as a bar chart.
- A pairplot is created to visualize the relationship between variables in the "model_data" dataset.

### Then I have perform a regression analysis on the input data using three models: Linear Regression, KNeighbors Regressor, and Random Forest Regressor.

#### 1.Linear Regression model:

- A Linear Regression model object is created using the scikit-learn library.
- The model is fit on the training data (X_train and y_train) using the fit method.
- The accuracy of the model is then evaluated on the test data (X_test and y_test) and validation data (X_val and y_val) using the r2_score function.

#### 2.KNeighbors Regressor model:

- A KNeighbors Regressor model object is created using the scikit-learn library.
- The model is fit on the training data (X_train and y_train) using the fit method.
- The accuracy of the model is then evaluated on the test data (X_test and y_test) and validation data (X_val and y_val) using the r2_score function.

#### 3.Random Forest Regressor model:

- A Random Forest Regressor model object is created using the scikit-learn library.
- The model is fit on the training data (X_train and y_train) using the fit method.
- The accuracy of the model is then evaluated on the test data (X_test and y_test) and validation data (X_val and y_val) using the r2_score function.
- The feature importance of the model is also calculated and stored in a dataframe.

#### 4.Prediction :

- Two dataframes are created to store the actual and predicted values for both the test data and validation data.
- The feature importance dataframe is also created to store the feature and its corresponding importance for the Random Forest Regressor model.
- Finally, the Non_Discount_data is updated with the predicted discount value using the Random Forest Regressor model.

### We observe that there is a high imbalance in the magnitude of data for each feature. The data for each feature varies significantly over the range. To improve the performance of the model, we can consider scaling the data using log transformation. This transformation can help reduce the impact of outliers and bring the data to a more comparable magnitude, thus improving the performance of the model.

### I have applied logarithmic scaling to the features of the training, testing and validation data. The purpose of this transformation is to make the data more normally distributed and easier to model. The logarithm is applied to the values in the feature column and the result is stored in the same column. A small value eps (0.001) is added to the values before taking the logarithm to avoid taking the logarithm of zero.

### After scaling the data, We noticed that the magnitude of each feature is more balanced and the distribution is closer to a normal distribution. This is important because some machine learning models are sensitive to the scale of the input features. By log transforming the data, we improved the alignment with a normal distribution, which can improve the performance of our model.

### This Scaling Has Improved the Model Performance With Following Result:
- The accuracy of the Linear Regression model has improved after taking the log of the data. Before the transformation, the test accuracy was 0.106 and validation accuracy was 0.100. After the transformation, the test accuracy increased to 0.164 and validation accuracy increased to 0.162.
- The accuracy of the KNeighbors Regressor model has improved after transforming the features. The test accuracy improved from 0.714 to 0.735 and the validation accuracy improved from 0.705 to 0.733.
- The Random Forest Regressor model accuracy before taking log of the features was around 0.8146 for the test data and 0.8122 for the validation data. After taking log of the features, the model accuracy was around 0.8144 for the test data and 0.8124 for the validation data. As we can see, the difference in accuracy is very minimal, indicating that taking log of the features did not have a significant impact on the model's accuracy.


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
