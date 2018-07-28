---
title: TensorFlow vs. the competition
layout: page
comments: true
social-share: true
show-avatar: true
---

TensorFlow competes with a slew of other machine learning frameworks. PyTorch, CNTK, and MXNet are three major frameworks that address many of the same needs. Below I’ve noted where they stand out and come up short against TensorFlow.

* **PyTorch**, in addition to being built with Python, and has many other similarities to TensorFlow: hardware-accelerated components under the hood, a highly interactive development model that allows for design-as-you-go work, and many useful components already included. PyTorch is generally a better choice for fast development of projects that need to be up and running in a short time, but TensorFlow wins out for larger projects and more complex workflows.

* **CNTK**, the Microsoft Cognitive Toolkit, like TensorFlow uses a graph structure to describe dataflow, but focuses most on creating deep learning neural networks. CNTK handles many neural network jobs faster, and has a broader set of APIs (Python, C++, C#, Java). But CNTK isn’t currently as easy to learn or deploy as TensorFlow.

* **Apache MXNet**, adopted by Amazon as the premier deep learning framework on AWS, can scale almost linearly across multiple GPUs and multiple machines. It also supports a broad range of language APIs—Python, C++, Scala, R, JavaScript, Julia, Perl, Go—although its native APIs aren’t as pleasant to work with as TensorFlow’s.