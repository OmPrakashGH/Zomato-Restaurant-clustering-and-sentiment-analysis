# Zomato Restaurant Clustering and Sentiment Analysis

<img src="https://resize.indiatvnews.com/en/resize/newbucket/1200_-/2021/07/zomato-2-1627023112.jpg" width="1000" height="500"/>

## Introduction

Zomato is an Indian restaurant aggregator and food delivery start-up. It provides information, menus and user-reviews of restaurants, and also has food delivery options from partner restaurants in select cities. India is quite famous for its diverse multi cuisine available in a large number of restaurants and hotel resorts, which is reminiscent of unity in diversity. Restaurant business in India is always evolving. More Indians are warming up to the idea of eating restaurant food whether by dining outside or getting food delivered. The growing number of restaurants in every state of India has been a motivation to inspect the data to get some insights, interesting facts and figures about the Indian food industry in each city. So, this project focuses on analysing the Zomato restaurant data for each city in India. This project mainly focuses on analyzing the Zomato restaurants data to get some insights by performing clustering and sentiment analysis.

### Clustering

Clustering is basically a type of unsupervised learning method. An unsupervised learning method is a method in which we draw references from datasets consisting of input data without labeled responses.

### Sentiment analysis

<img src="https://www.reputationx.com/hubfs/what-is-sentiment-analysis-cover.jpg" width="600" height="200"/>

Sentiment analysis, also referred to as opinion mining, is an approach to natural language processing (NLP) that identifies the emotional tone behind a body of text.
This is a popular way for organizations to determine and categorize opinions about a product, service, or idea. It involves the use of data mining, machine learning (ML) and artificial intelligence (AI) to mine text for sentiment and subjective information.

## Project Objectives

* To get insights from data by performing EDA.
* To cluster the restaurants into different segments by using various clustering algorithms.
* To analyze the sentiment of the reviews given by the customers in the data. 

## Dataset Information

### Zomato Restaurant names and Metadata

Name : Name of Restaurants

Links : URL Links of Restaurants

Cost : Per person estimated Cost of dining

Collection : Tagging of Restaurants w.r.t. Zomato categories

Cuisines : Cuisines served by Restaurants

Timings : Restaurant Timings

### Zomato Restaurant reviews

Restaurant : Name of the Restaurant

Reviewer : Name of the Reviewer

Review : Review Text

Rating : Rating Provided by Reviewer

MetaData : Reviewer Metadata - No. of Reviews and followers

Time: Date and Time of Review

Pictures : No. of pictures posted with review

## Feature Engineering for Clustering

From the merged dataset the metadata column has been separated the reviews and followers into two separate columns. Then we have taken some selected columns for the
clustering like ‘Name’, ‘Cost’, ‘Mean Rating’, ‘Mean Followers’. We have aggregated the ‘Rating’ and ‘Number of followers’ column to make it a single value for each
restaurant.

## Feature Engineering for Sentiment analysis

For sentiment analysis we have taken some selected columns from the merged dataset, like ‘Name’, ‘Review’, and ‘Rating’ columns. Then we grouped the ‘Rating’
column into two parts, one with rating 0 to 3 as negative (0) and rating 4 to 5 as positive (1) class. Then we have removed the stop words and punctuations from the
‘Review’ column followed by stemming and vectorization.

## Models used for Sentiment analysis

Naive Bayes Classifier

Logistic Regression

XGBoost

SVM

## Conclusions

From the EDA we have explored popular cuisines and collections, costliest and cheapest restaurants, top rated and worst rated restaurants, most reviewed and most followed restaurants and the restaurants with most positive and most negative reviews.

The optimal number of clusters by taking two variables at a time are either three or four and the optimal number of clusters by taking all variables at a time is four.

From sentiment analysis it is found that logistics regression and SVM are the two most appropriate models with accuracy of nearly 87%.
