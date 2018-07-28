---
title: Introduction to Approach Machine Learning problems
layout: page
comments: true
social-share: true
show-avatar: true
---

***One of the main tasks of computers is to automate human tasks. Some of these tasks are simple and repetitive, such as “move X from A to B.” It gets far more interesting when the computer has to make decisions about problems that are far more difficult to formalize. That is where we start to encounter basic machine learning problems.***

Historically, such algorithms were built by scientists or experts that had intimate knowledge of their field and were largely based on rules. With the explosion of computing power and the availability of large and diverse data sets, the focus has shifted toward a more computational approach.

Most popularized machine learning concepts these days have to do with neural networks, and in my experience, this created the impression in many people that neural networks are some kind of a miracle weapon for all inference problems. Actually, this is quite far from the truth. In the eyes of the statistician, they form one class of inference approaches with their associated strengths and weaknesses, and it completely depends on the problem whether neural networks are going to be the best solution or not.

First, however, let us spend some effort showing why you should be more circumspect than to automatically think “neural network” when faced with a machine learning problem.

***Pros and Cons of Neural Networks***
With neural networks, the inference is done through a weighted “network.” The weights are calibrated during the so-called “learning” process, and then, subsequently, applied to assign outcomes to inputs.

As simple as this may sound, all the weights are parameters to the calibrated network, and usually, that means too many parameters for a human to make sense of.

So we might as well just consider neural networks as some kind of an inference black box that connects the input to output, with no specific model in between.

Let us take a closer look at the pros and cons of this approach.

**Advantages of Neural Networks**

* The input is the data itself. Usable results even with little or no feature engineering.
* Trainable skill. With no feature engineering, there is no need for such hard-to-develop skills as intuition or domain expertise. Standard tools are available for generic inferences.
* Accuracy improves with the quantity of data. The more inputs it sees, the better a neural network performs.
* May outperform classical models when there is not full information about the model. Think of public sentiment, for one.
* Open-ended inference can discover unknown patterns. If you use a model and leave a consideration out of it, it will not detect the corresponding phenomenon. Neural networks might.

Successful neural network example: Google’s AI found a planet orbiting a distant star—where NASA did not—by analyzing accumulated telescope data.

**Disadvantages of Neural Networks**

* **They require a lot of (annotated!) data**. First, this amount of data is not always available. Convergence is slow. A solid model (say, in physics) can be calibrated after a few observations—with neural networks, this is out of the question. Annotation is a lot of work, not to mention that it, in itself, is not foolproof.
* **No information about the inner structure of the data.** Are you interested in what the inference is based on? No luck here. There are situations where manually adjusting the data improves inference by a leap, but a neural network will not be able to help with that.
* **Overfitting issues** . It happens often that the network has more parameters than the data justifies, which leads to suboptimal inference.
* **Performance depends on information**. If there is full information about a problem, a solid model tends to outperform a neural network.
* **There are sampling problems.** Sampling is always a delicate issue, but with a model, one can quickly develop a notion of problematic sampling. Neural networks learn only from the data, so if they get biased data, they will have biased conclusions.

An example of failure: A personal relation told me of a major corporation (that I cannot name) that was working on detecting military vehicles on aerial photos. They had images where there were such vehicles and others that did not. Most images of the former class were taken on a rainy day, while the latter were taken in sunny weather. As a result, the system learned to distinguish light from shadow.

The fact that their popularity outshines all other statistical methods in the eyes of the public has likely more to do with corporate governance than anything else.

Training people to use standard tools and standardized neural network methods is a far more predictable process than hunting for domain experts and artists from various fields. This, however, does not change the fact that using a neural network for a simple, well-defined problem is really just shooting a sparrow with a cannon: It needs a lot of data, requires a lot of annotation work, and in return might just underperform when compared to a solid model. Not the best package.

Still, there is huge power in the fact that they “democratize” statistical knowledge. Once a neural network-based inference solution is viewed as a mere programming tool, it may help even those who don’t feel comfortable with complex algorithms. So, inevitably, a lot of things are now built that would otherwise not exist if we could only operate with sophisticated models.

**Approaching Machine Learning Problems**

When approaching machine learning problems, these are the steps you will need to go through:

* Setting acceptance criteria.
* Cleaning your data and maximizing ist information content.
* Choosing the most optimal inference approach.
* Train, test, repeat