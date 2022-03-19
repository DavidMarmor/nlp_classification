# Project 2 - Ames Housing Data and Kaggle Challenge

# Problem Statement and Background 

Buying and selling a home is a big step in people's lives. It can be hard for both the buyer and the seller to know what a fair price of the house is. A model that could predict how much a house will be sold for based on a variety of features would be a valuable resorce if it had good predictive success. Then buyers and sellers could feel comfortable knowing about what a given house should go for. Housing prices vary across cities and states so it makes sense to have different models in different areas. In this project I will build a model for sale price of houses in Ames Iowa based on data collected on house sales in the city between 2006 and 2010. I will using linear, ridge, and lasso regression to try and model sale prices. The models will be evaluated using R squared score which measures the amount of variation in sale price that can be explained by the model. In addition inference will be used to determine the relationships between sale price and variables. That allows home buyers to find homes that they believe are undervalued because they care more about certain features then the general public. 

# Data Dictionary 

|Feature|Description|
|---|---|
|**sale price**|price of sale in dollars.| 
|**Overall Qual**|Material and finish of the house rated 1-10|
|**Gr Liv Area**|above grade ground living area in square feet|
|**Garage Area**|Garage size in square feet|
|**Total Bsmt SF**|basement area in square feet| 
|**MasVnrArea**|Masonry Veneer area in square feet|
|**Fireplaces**|number of fireplaces in house| 
|**NridgHt**|is the house in the northridge heights area|
|**BsmtFin SF**|finished area of basement in square feet| 

# EDA 

To start with the dataset had 81 features. I filled in NAs with reasonable values based on the data dictionary. I then created dummy variables for categorical features. To select the features that would be used for the regression a heatmap was created to find the variables that had a strong correlation with sale price. Any variable with a correlation with sale price greater than 0.4 or less than -0.4 was studied to decide if it belonged in the model. Of the 14 variables that were remaining 6 were removed for either multicollinearity or not having a linear relationship with sale price. That left the 8 variables listed in the data dictionary above. 

# Linear Regression. 

After scaling data and doing the train test split the regression was performed. The model has a 0.85 R squared score on the training set and a 0.84 score on the testing set. This was compared to a ridge regression and a lasso regression. All three regressions had similar model metrics. Because the linear regression is the easiest to explain to our residents it is the one to use.

However to perform inference LINE conditions have to be met and the variance of residuals had a clear pattern for houses that were sold for more than 300000 dollars. So a new model was performed on only houses that sold for under that price. That model allows us to perform inference for houses in that range. The most important factors are overall quality and ground living area. 

# Conclusion and Further Work 

We have successfully come up with a model that can explain over 80% of the variation in sale prices and does not seem to suffer from underfitting and overfitting. We can use the model to estimate how much a house will go for. This will allow us to provide reasonable estimates to prospective buyers and sellers. By providing it to the public we can perform a service to the people in Ames. We also might be able to get people to move from neighbooring towns if they find our model makes the house buying process easier and less stressful. 

Our inferential model allows people to interpret coefficients for houses less then 300000 dollars. By interpreting the coefficients home buyers can see how various factors impact the price of a house.

Further work needs to be done to come up with an inferential model that works on houses that sell for over 300000 dollars. That way there will be a model for all prosective house buyers to perform inference on.  

Further work could be done by running a grid search and refining the model. In addition collecting more information, might make the model even better. Also we could provide the model to other cities so they can tweak the model for their cities.






