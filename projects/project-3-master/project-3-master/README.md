# Executive Summary 

# Problem Statement 

Our client Major League Baseball (MLB) wants to improve their fan outreach. By getting fans excited about the game they hope to increase attendence and generate other types of revenue. They want to know if the same type of outreach will work for different types of fans. We will be comparing more analytically inclined fans to fans as a whole. We will create a model that tries to predict whether a post comes from the mlb subreddit or the sabermetrics subreddit. The mlb subreddit is for all MLB fans. The sabermetric subreddit is specifically for fans interested in a more analytical outlook. If the model can identify the differences that means that outreach should probably be tailored depending on which group it is for. And using the model we create MLB will be able to study the differences. For the model to be useful it will need to beat the baseline on new data. 

To create the model we will use ada boosting, random forests, logistic regression, and naive bayes. There are advantages to using these models. Logistic regression and naive bayes take relatively less computing power. It also tends not to overfit the data. Random Forests and adaboosting tend to perform well and correct overfitting issues in decision trees. The models will be evaluated using accuracy since one type of error is not any better or worse then the other in this case. We will also look at other metrics to get a full picture of how the model is doing. Recall is a measure of what percentage of positives the model correctly predicts. Precision is a measure of how accurate the model is when it predicts a positive. Specificity is a measure of what percentage of negatives the model correctly predicts. Negative predictive value is a measure of how accurate the model is when it predicts a negative. In our case a postive is a post from the sabermetrics subreddit and a negative is a post from the mlb one.

In addition for each model we will try the CountVectorizer and TfidfVectorizer to see which performs better.

# Analysis 

|model|Vectorizer|Accuracy|Recall|Precision|Specificity|Negative Predictive Value|
|---|---|---|---|---|---|---|
|adaboost|CountVectorizer|0.89|0.85|0.92|0.93|0.86|
|random forests|CountVectorizer|0.89|0.90|0.88|0.89|0.90|
|logistic regression|Tfid Vectorizer|0.92|0.92|0.92|0.93|0.92|
|naive bayes|Tfid Vectorizer|0.93|0.95|0.91|0.91|0.95| 

The adaboost model is the least accurate of the 4. It has a larger numbe of false negatives. This is where the model predicts that the post is from the mlb subreddit but it is actually from the sabermetric one. The random forests model has a slightly higher accuracy than the adaboost model. It also has a similar number of false positives and false negatives. However it has the most severe overfitting. The accuracy on the test data is greater than 0.99. The logistic regression model has an accuracy of over 0.9 which the first two models do not. It also has a similar number of false positives and false negatives. The naive bayes is the most accurate model of the 4. It does have a higher rate of false positives than the logistic regression model. However it has the least overfitting of any of the models. 

Overall all the models beat the baseline which is 0.51. That suggests that there is a difference between the two subreddits.


# Conclusion 

We were successfully able to model the difference between our two subreddits. That means there are differences between how the sabermetric community talks about baseball compared to MLB fans at large. MLB might want to have a seperate outreach for them to have the biggest impact.

The naive bayes model with TfidVectorizer was the most effective model at accurately predicting the test data and had the least overfitting. Therefore it is the model that we will use going forward to study this issue. 

Now that we have a model that can predict which subreddit the post comes from we can do more research on the differences between the two. Then we can recommend how to appeal to each group individually. Though targeted ads we hope to grow greater fan interest and engagement.

Fans of sabermetrics are not the only sub group of MLB fans. Running this model comparing the mlb subreddits to other baseball subreddits might give us a good idea of other groups of fans who might warrent targeted outreach

Other further work can be done improving the model and trying other models. Other models like SVM, gradient boosting, and neural networks may have gotten even better results. Also there are always more hyperparameters to tune. However, overall our model has an accuracy of over 90% so we feel comfortable using it going forward.