# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Capstone Project: News Text Summarization

#### Note:
Please unzip glove6b.z01 file before running the codes to get the GloVe embeddings. Otherwise codes will encounter an error. The txt file is too huge to push onto GitHub.

## Problem Statement

To make use of automatic text summarization on the latest news articles to create short and concise summaries in order to save time on reading.

## Executive Summary

Time is money, and with the amount of content being published these days, we do not have the time to be reading everything. This project aims to scrape for the latest news and make use of automatic text summarization to investigate how best to provide a short and concise summary of the article so reades are able to save time having to read the whole article.

In this project, we will mainly be exploring extractive text summarization algorithms and the evaluation metric will be based on Rouge Score.

### News Sources:
- Associated Press News ('https://apnews.com/')
- BBC ('https://www.bbc.com/news')
- NPR ('https://www.npr.org/')

### Dataset:
https://www.kaggle.com/sunnysai12345/news-summary

### Contents:
- Importing and Data Cleaning
- Exploratory Data Analysis
- Modelling
- Evaluation
- Scraped News Summary
- Conclusion

### Findings:
Rouge-1 Score

||lede_3|lexrank|luhn|lsa|textrank|edmundson|glove_textrank|
|---|---|---|---|---|---|---|---|
|recall|0.513883|0.465951|0.494760|0.376341|0.483477|0.376341|0.471846|
|precision|0.397336|0.327083|0.282885|0.298557|0.270421|0.298557|0.296988|
|f1|0.439107|0.377744|0.355731|0.327353|0.342800|0.327353|0.359630|


## Conclusion

From the mean results of the Rouge Score for each article, it can be seen that the lede-3, which is our baseline model, performs better than that all the other algorithms implemented. The lede-3 method is basically summarization by using the first few words or sentences of a text. The reason why the lede-3 is so competitive and may even outperform the other algorithms could due to the nature of the way news articles are written, whereby the main points can usually be found at the start of the article.

When it comes to automatic text summarization, there are so many other methods and applications for it. So far, we have only dealt with some of the extractive text summarization algorithms on news articles, and that is only like a small little fish in the big ocean. Perhaps if we were to look at other kinds of documents, such as reviews or whatnot, the other extractive text summarization algorithms might perform better than the baseline model, lede-3. 

Nevertheless, other types of text summarization should also be explored, such as abstractive text summarization, though it is noted that it is computationally expensive. A huge dataset and lots of time would be needed to train the model in order for it to perform optimally. Another strategy would be to use a mixed strategy of both extractive and abstractive text summarization methods.

Ultimately, since the the lede-3 baseline model is able to show the best results, we will proceed with using it on our scraped news data until we are able to find other algorithms that can outperform the baseline model. Sometimes, the simpler model will do just fine too, but definitely, more research can be done on text summarization to find better algorithms.
