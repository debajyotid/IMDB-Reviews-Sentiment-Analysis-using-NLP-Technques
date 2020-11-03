# IMDB-Reviews-Sentiment-Analysis-using-NLP-Technques
## Introduction

This exercise uses the data from Kaggle's [IMDB Movie reviews](https://www.kaggle.com/c/word2vec-nlp-tutorial/data) competition.

In this tutorial competition, we dig a little "deeper" into sentiment analysis. **Google's Word2Vec** is a deep-learning inspired method that focuses on the meaning of words. **Word2Vec attempts to understand meaning and semantic relationships among words**. It works in a way that is similar to deep approaches, such as recurrent neural nets or deep neural nets, but is computationally more efficient. This tutorial focuses on Word2Vec for **sentiment analysis**.

Sentiment analysis is a challenging subject in machine learning. People express their emotions in language that is often obscured by sarcasm, ambiguity, and plays on words, all of which could be very misleading for both humans and computers. In this tutorial we explore how Word2Vec can be applied to a similar problem.

## Data Set

The labeled data set consists of 50,000 IMDB movie reviews, specially selected for sentiment analysis. The sentiment of reviews is binary, meaning the IMDB rating < 5 results in a sentiment score of 0, and rating >=7 have a sentiment score of 1. No individual movie has more than 30 reviews. The 25,000 review labeled training set does not include any of the same movies as the 25,000 review test set. In addition, there are another 50,000 IMDB reviews provided without any rating labels.

**File descriptions**

- labeledTrainData - The labeled training set. The file is tab-delimited and has a header row followed by 25,000 rows containing an id, sentiment, and text for each review. This is available as **`labeledTrainData.tsv.zip`**
- testData - The test set. The tab-delimited file has a header row followed by 25,000 rows containing an id and text for each review. Your task is to predict the sentiment for each one. 
- unlabeledTrainData - An extra training set with no labels. The tab-delimited file has a header row followed by 50,000 rows containing an id and text for each review. 
- sampleSubmission - A comma-delimited sample submission file in the correct format.

### Data fields

- **id** - Unique ID of each review
- **sentiment** - Sentiment of the review; 1 for positive reviews and 0 for negative reviews
- **review** - Text of the review

## Acknowledgements

This dataset was collected in association with the following publication:

Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, and Christopher Potts. (2011). "Learning Word Vectors for Sentiment Analysis." The 49th Annual Meeting of the Association for Computational Linguistics (ACL 2011). (link)

Please email the author of that paper if you use the data for any research applications. The tutorial was developed by Angela Chapman during her summer 2014 internship at Kaggle.

## Metric

Submissions are judged on **area under the ROC curve**. 

### Submission Instructions

You should submit a comma-separated file with 25,000 row plus a header row. There should be 2 columns: "id" and "sentiment", which contain your binary predictions: 1 for positive reviews, 0 for negative reviews. For an example, see "sampleSubmission.csv" on the Data page. 

#### id,sentiment
- 123_45,0 
- 678_90,1
- 12_34,0
