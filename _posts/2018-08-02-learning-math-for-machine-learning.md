---
title: Learning Math for Machine Learning
layout: page
comments: true
social-share: true
show-avatar: true
---

It’s not entirely clear what level of mathematics is necessary to get started in machine learning, especially for those who didn’t study math or statistics in school.

In this piece, my goal is to suggest the mathematical background necessary to build products or conduct academic research in machine learning. These suggestions are derived from conversations with machine learning engineers, researchers, and educators, as well as my own experiences in both machine learning research and industry roles.

To frame the math prerequisites, I first propose different mindsets and strategies for approaching your math education outside of traditional classroom settings. Then, I outline the specific backgrounds necessary for different kinds of machine learning work, as these subjects range from high school-level statistics and calculus to the latest developments in probabilistic graphical models (PGMs). By the end of the post, my hope is that you’ll have a sense of the math education you’ll need to be effective in your machine learning work, whatever that may be!

**Getting Started**

As soft prerequisites, we assume basic comfortability with linear algebra/matrix calculus (so you don’t get stuck on notation) and introductory probability. We also encourage basic programming competency, which we support as a tool to learn math in context. Afterwards, you can fine-tune your focus based on the kind of work you’re excited about.

How to Learn Math Outside of School I believe the best way to learn math is as a full-time job (i.e. as a student). Outside of that environment, it’s likely that you won’t have the structure, (positive) peer pressure, and resources available in the academic classroom.

To learn math outside of school, I’d recommend study groups or lunch and learn seminars as great resources for committed study. In research labs, this might come in the form of a reading group. Structure-wise, your group might walk through textbook chapters and discuss lectures on a regular basis while dedicating a Slack channel to asynchronous Q&A.

Culture plays a large role here — this kind of “additional” study should be encouraged and incentivized by management so that it doesn’t feel like it takes away from day-to-day deliverables. In fact, investing in peer-driven learning environments can make your long-term work more effective, despite short-term costs in time.

**Math and Code**

Math and code are highly intertwined in machine learning workflows. Code is often built directly from mathematical intuition, and it even shares the syntax of mathematical notation. In fact, modern data science frameworks (e.g. NumPy) make it intuitive and efficient to translate mathematical operations (e.g. matrix/vector products) to readable code.

I encourage you to embrace code as a way to solidify your learning. Both math and code depend on precision in understanding and notation. For instance, practicing the manual implementation of loss functions or optimization algorithms can be a great way to truly understanding the underlying concepts.

As an example of learning math through code, let’s consider a practical example: implementing backpropagation for the ReLU activation in your neural network (yes, even if Tensorflow/PyTorch can do this for you!). As a brief primer, backpropagation is a technique that relies on the chain rule from calculus to efficiently compute gradients. To utilize the chain rule in this setting, we multiply upstream derivatives by the gradient of ReLU.

Resources

• [Best practices for ML Engineering](https://developers.google.com/machine-learning/guides/rules-of-ml/) by Martin Zinkevich, Research Scientist at Google.

**Learning Math as You Need It**

Diving headfirst into a machine learning workflow, you might find that there are some steps that you get stuck at, especially while debugging. When you’re stuck, do you know what to look up? How reasonable are your weights? Why isn’t your model converging with a particular loss definition? What’s the right way to measure success? At this point, it may be helpful to make assumptions about the data, constrain your optimization differently, or try different algorithms.

Often, you’ll find that there’s mathematical intuition baked into the modeling/debugging process (e.g. selecting loss functions or evaluation metrics) that could be instrumental to making informed, engineering decisions. These are your opportunities to learn!

Rachel Thomas from Fast.ai is a proponent of this “on-demand” method — while educating students, she found that it was more important for her deep learning students to get far enough to become excited about the material. Afterwards, their math education involved filling in the holes, on-demand.