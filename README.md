# Outlet Sales Price Pediction
**Jon Messier**\
**Dec, 2022**\
As a requirement for Coding Dojo Data Science w/ Python.

## Comparing Linear Regression and Decision Tree models
The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.  We will do this by looking at 2 different models of the Outlet_Sales Data

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
- Linear Regression
 - R^2 =
 - RSME =
- Decision Tree
 - R^2 = 
 - RSME =
The evaluation showed a preference to the ____ Machine Learning Model

## Recomendations
## Limitations
## Further Information
