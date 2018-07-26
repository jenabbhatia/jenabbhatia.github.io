---
title: Simple Example of Neural Network
layout: page
comments: true
social-share: true
show-avatar: true
---

A simple example of applying neural networks is by predicting x1 AND x2, which is the logical 'and' operator and is only true if both x1 and x2 are 1.

The graph of our functions will look like:
 
![Graph_function](/graph_fun.png){:class="img-responsive"}

Remember that x0 is our bias variable and is always 1.

Let's set our first theta matrix as:

![Theta_matrix](/first_theta_matrix.png){:class="img-responsive"}

This will cause the output of our hypothesis to only be positive if both x1 and x2  are 1. In other words:

![Hypothesis](/hypothesis.png){:class="img-responsive"}

So we have constructed one of the fundamental operations in computers by using a small neural network rather than using an actual AND gate. Neural networks can also be used to simulate all the other logical gates. The following is an example of the logical operator 'OR', meaning either x1  is true or x2 is true, or both:

![OR_Function](/OR_function.png){:class="img-responsive"}