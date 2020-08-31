# NLP-Topic-Modeling-and-Sentiment-Analysis-of
Twitter Customer Support Topic Modeling and Sentiment Analysis

This project explores Customer Support Conversations on Twitter with Sentiment Analysis, Topic Modeling
## Database
database used : https://www.kaggle.com/thoughtvector/customer-support-on-twitter/download

## Idea
Database contains twitter support data. I have used k-mean clustering for unsupervised sentiment analysis and Non-negative Matrix Factorization (NMF) for topic modeling.

#### Unsupervised sentiment Analysis idea:

The negative and positive words usually are surrounded by similar words. This means that if we would have movie reviews dataset, word ‘boring’ would be surrounded by the same words as word ‘tedious’, and usually such words would have somewhere close to the words such as ‘didn’t’ (like), which would also make word didn’t be similar to them. On the other hand, it would be unlikely to have happened, that word ‘tedious’ had more similar surrounding to word ‘exciting’, than to word ‘boring’. With such assumption, words could form clusters (based on similarity of their surrounding) of negative words that have similar surroundings, positive words that have similar surroundings, and some neutral words that end up between them (such as ‘movie’). 

I have used word2vec model to encode and used k-mean clustering to make sentiment dictonary. This sentiment scores of words used with tfidf scores to get sentiment or frustration of customer

#### Non-negative Matrix Factorization (NMF) for topic modeling.
Non-Negative Matrix Factorization (NMF) is an unsupervised technique so there are no labeling of topics that the model will be trained on. The way it works is that, NMF decomposes (or factorizes) high-dimensional vectors into a lower-dimensional representation. These lower-dimensional vectors are non-negative which also means their coefficients are non-negative.

## Repo notebook info
Data folder has database link download and put it there

data_extraction.ipynb - contains data cleaning and and data extraction codes. (run this notebook first)

sentiment_analysis.ipynb - have implementation of unsupervised sentiment analysis

topic_modeling.ipynb - have NMF topic modeling implementation

