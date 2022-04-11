# Project 4 

# Problem Statement 

Can we predict the revenue of a restaurant? 

# Analysis 

The models that were run were linear regression, random forests regression, knn, and svr. The variables included in the final model were all dummy variables. They were whether the restaurant was a food court, whether the restaraunt was located in instanbul, whether the restaraunt was located in Ankara, and whether the restaurant openned in the year 2000. 

The knn and svr models had negative r squared scores on the test data. which means they were worse then the baseline. The linear regression and random forests models both had an r squared score on training data of 0.28. However the random forest model did better on the testing data with a score of 0.16. Both models that did better than baseline are very overfit and not much better then baseline.

# Conclusion 

While we did better then the baseline it is hard to say that we can predict restaurant revenue. The random forests model is the best model. However it has a very poor r squared score and is overfit.

There are many things that could be done with more time to try and improve the models. I could try a neural network. I could use a gridsearch to find the best hyperparameters for the variables I used. I am not sure any of these things would help too much. From the correlation matrix it is apparent that none of the features are highly correlated with the target variable. However, while the model still probably would not be great, it would hopefully be better than it is now.