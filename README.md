# Project 2: Ames Housing Data 

#### Michael Xiao, General Assembly SG-DSI-8

#### June 7, 2019

## Problem Statement
#### What features drive the price of houses in Ames, Iowa and where are they located?

## Executive Summary
In Project 2, we worked with Kaggle data on predicting sale prices of house in Ames, Iowa to understand which features have a significant impact on housing prices. Working with over 80 various features, we aim to construct a model that can predict the sale price of houses based on selected features that play a significant role in the valuation. 

We compared against three models in this challenge, namely the linear regression model, the lasso model, and the ridge model. Our linear regression model acts as a baseline of R-squared we must aim to achieve. Upon the first glance, the R-squared came to be an unsatisfactory score of -2.61. This means that there are a lot of 'noise' in our data and that our data is not explaining sale price well (at this point, we have 145 features including dummies). Upon running our lasson and ridge model, both models returned a R-squared score of 0.89 which can be perceived as the model being able to explain 89% of the variance in the data. We also streamlined our features down to twenty features. Thereafter, we used our features to predict sale price for our test set.

The size of ground living area, overall quality of the house, total basement square feet and kitchen quality appear to add most value to a home sale price. On the other hand, houses without a basement, townhouse end units, and older property will significantly hurt the value of a home. Our model predicts that neighbourhoods such as Stone Brook, Northridge Heights, Green Hills, Northridge and Crawford have a high coefficient to sale price. This means houses in these neighbourhoods are likely be be pricier than other cities. Our results are similar to that of what a regular homeowner will look out for when buying or selling a property. 

Our data has also shown that having a fireplace in Iowa will significantly increase the valuation of house price. Quality of the fireplace plays a part of the sale price as well. Thus, the more quality fireplaces a house have, the higher the value. 
As Ames have an average annual temperature of 49.45°F (9.69°C), it is no wonder fireplaces is an important feature to sale price.

Data Dictionary: http://jse.amstat.org/v19n3/decock/DataDocumentation.txt

Added features:
['prop_age'] = age of property [['yr_sold'] - ['year_built']]
['pool'] = area and quality of pool [['pool_area'] * ['pool_qc']]
['bsmt'] = quality and condition of basement [['bsmt_qual'] * ['bsmt_cond']]
['fireplace'] = number and quality of fireplaces [['fireplaces'] * ['fireplace_qu']]
['garage_aes'] = aesthetics of garage [['garage_finish'] * ['garage_qual'] * ['garage_cond']]




