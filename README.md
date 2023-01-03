# Outlet Sales Price Pediction
**Jon Messier**\
**Dec, 2022**\
As a requirement for Coding Dojo Data Science w/ Python.

![BM Graphic](https://www.analyticsvidhya.com/wp-content/uploads/2016/02/Comp-4.jpg)

## Comparing Regression Models
The goal of this project is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.  We will do this by looking at a few different models of the Outlet_Sales Data.  I tune each model to one or more hyperparameters to improve test data's fit to the model.  The models explored will be:
 - Linear Regression
 - Dummy Regression
 - Decision Tree
 - Bagged Tree
 - Random Forest
 
For each of the models used, the Mean Absolute Error (MAE), Mean Standard Error (MSE), Root Mean Squared (RMSE), and the coefficient of determination (R2) will be calculated and compared with each model.


## Data
Raw data found [HERE](https://drive.google.com/uc?id=1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw)

## Data Dictionary
<table><tbody><tr><td><strong>Variable Name</strong></td><td><strong>Description</strong></td></tr><tr><td>Item_Identifier</td><td>Unique product ID</td></tr><tr><td>Item_Weight</td><td>Weight of product</td></tr><tr><td>Item_Fat_Content</td><td>Whether the product is low fat or regular</td></tr><tr><td>Item_Visibility</td><td>The percentage of total display area of all products in a store allocated to the particular product</td></tr><tr><td>Item_Type</td><td>The category to which the product belongs</td></tr><tr><td>Item_MRP</td><td>Maximum Retail Price (list price) of the product</td></tr><tr><td>Outlet_Identifier</td><td>Unique store ID</td></tr><tr><td>Outlet_Establishment_Year</td><td>The year in which store was established</td></tr><tr><td>Outlet_Size</td><td>The size of the store in terms of ground area covered</td></tr><tr><td>Outlet_Location_Type</td><td>The type of area in which the store is located</td></tr><tr><td>Outlet_Type</td><td>Whether the outlet is a grocery store or some sort of supermarket</td></tr><tr><td>Item_Outlet_Sales</td><td>Sales of the product in the particular store. This is the target variable to be predicted.
<a href="https://github.com/ShauryaBhandari/Bigmart-Sales-Prediction#why-does-the-the-problem-need-to-be-solved" id="user-content-why-does-the-the-problem-need-to-be-solved" class="anchor" aria-hidden="true" target="_blank"></a></td></tr></tbody></table>


## Data Preparation
To prepare this data, the data was cleaned, and the following processes were performed:
- Review Numerical entries for outliers - None found
- Review and replace Categorical entry inconsistancies - Inconsistancies found in `Item_Fat_Content`
- Review Missing Data - Missing entries are imputed with SimpleImputer in the preprocessing pipelines
- Review `Dtypes` - All data types look appropriate
- Missing values were replaced according to:
 - Numerical - Mean
 - Nominal - replaced with 'UNK'
 - Ordinal - replaced with `most_frequent`

## Exploratory Data Analysis
Using boxplots and histograms we saw that the highest performing Outlet type was the `Supermarket Type1`.\  
![Outlet Type](https://drive.google.com/uc?id=16PauujXw0s-soOrVqFEGkK9k5_9dwgFy)

We also learned that the best selling products are:
- Fruits and Vegetables > $1.4M
- Snack Foods > $1.3M
- Houshold > $1M\

![Best Selling](https://drive.google.com/uc?id=16TIUSPQ2aMXsOS9kgLJeIDWt3fRbdvq-)


## Machine Learning Models/Evaluation
The data was split into train and test data and evaluated using the following models:
 - Linear Regression
 - Dummy (Mean) regression
 - Decision tree
 - Bagged tree
 - Random Forest

The evaluation showed a preference to the Random Forest Tree Machine Learning Model with a 60.4% fit to the test data
![Model Comparison](https://drive.google.com/uc?id=16cv5j2j08gb_ZS_bdUvmGxaIqAAOC8wB)


## Recomendations
Based on the evaluation of the models used, the recomendation to use a Random Forest Regression model tuned for max_depth to aid in Outlet_Sales.  This recomendation is based on the 60% fit to the test data.

## Limitations
1) Without directly communicating with the dataset owner, it is difficult to interpret some of the features.  `Item_Visibility` for example is simply a number, does a lower or high number mean the item is more visible?  Communication with stakeholders is key to modeling and understanding datasets. 
2) Missing data may impact the models fit to the data.  A cleaner set without as many missing values would be ideal.
3) Each of the models used in this analysis was tuned using only 1 hyperparameter.  With more time and resources fine tuning of models might produce a better fit. Considering the resource intensive process of training models, I assume that the fit is sufficient for priliminary analysis.  

## Further Information
This is my first project learning Data Science with python.  It was completed as part of my training with Coding Dojo - Data Science bootcamp.  I will continue to make small changes to this code and report as I progress in the class.
