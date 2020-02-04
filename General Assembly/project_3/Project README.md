# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Project 3: Reddit API


## Problem Statement

To use data scrapped from reddit and create a model that is able to alert us of troll posts(that should be on r/Jokes) instead of r/askscience.

## Executive Summary

Being a moderator on the subreddit r/askscience can be tiring when you have internet trolls constantly posting troll questions on the subreddit. This project aims to explore ways to create a model that is able to accurately and consistenly alert moderators of troll posts based on posts from r/Jokes.

## Conclusion

After thoroughly reviewing through all the metrics we have gathered as well as looking at the ROC curve, the recommended model to use would be the Multinomial Naive Bayes model alongside with the Count Vectorizer.

While the recommended model does not have the best results when you look at all the metrics and compare it against the other models, the results are not very far off. Having an Accuracy score of 0.8917 is already considered very high and is more than our baseline score. Ultimately, we would also not want our Accuracy score to be extremely high as it would probably be indicative of the model overfitting the data. Also with an AUC score of 0.9685, it tells us that the model does a good job of classifying our data points.

Another reason for recommending the Multinomial Naive Bayes Model with Count Vectorizer is because the Accuracy score for the test data set is the most consistent with the training data and the GridSearchCV mean score, which means that the model is able generalize better compared to the other models.

At the end of the day, it is not always about choosing the model that has the best metrics based on a single test, but to choose the model that is able to perform the most consistent.

## Moving Forward

As this model is trained on words which users post on reddit, it is important to constantly re-train the model as the words and lingo that people use tend to change with time.

Future steps we can look into to improve our classification model would perhaps be to integrate the length of the titles and selftext into our model. As mentioned earlier, titles and selftext on r/askscience generally tend to be longer than those on r/Jokes.
