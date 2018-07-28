---
title: Sentiment Analysis With Python
layout: page
comments: true
social-share: true
show-avatar: true
---

This is a demonstration of sentiment analysis using a NLTK 2.0.4 powered text classification process. It can tell you whether it thinks the text you enter below expresses positive sentiment, negative sentiment, or if it's neutral. Using hierarchical classification, neutrality is determined first, and sentiment polarity is determined second, but only if the text is not neutral.

![sentimentAnalysis](/sentiment_analysis.png){:class="img-responsive"}

**How Sentiment Analysis with Text Classification Works**

The english sentiment uses classifiers trained on both twitter sentiment as well as movie reviews from the data sets created by Bo Pang and Lillian Lee using nltk-trainer (also on bitbucket). The dutch sentiment is based on book reviews.

The results will be more accurate on text that is similar to original training data. If you get an odd result, it could be the words you've used are unrecognized. Try entering more words to improve accuracy.

**Sentiment Analysis Articles**

To read more about how it works, please read the following articles I've written about the process:

* Training a naive bayes classifier for sentiment analysis using movie reviews
* Calculating high information words for sentiment analysis

**Natural Language Sentiment Analysis API**

If you'd like to use this thru an API, please see the Sentiment Analysis API Docs.