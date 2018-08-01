---
layout: page
comments: true
social-share: true
show-avatar: true
title: 'Faust: Stream Processing for Python'
---

Faust is a stream processing library, porting the ideas from Kafka Streams to Python.

It is used at Robinhood to build high performance distributed systems and real-time data pipelines that process billions of events every day.

Faust provides both stream processing and event processing, sharing similarity with tools such as Kafka Streams, Apache Spark/Storm/Samza/Flink,

It does not use a DSL, it's just Python! This means you can use all your favorite Python libraries when stream processing: NumPy, PyTorch, Pandas, NLTK, Django, Flask, SQLAlchemy, ++

Faust requires Python 3.6 or later for the new async/await syntax, and variable type annotations.

Have a look:
[Faust:Stream processing for python](https://github.com/robinhood/faust)