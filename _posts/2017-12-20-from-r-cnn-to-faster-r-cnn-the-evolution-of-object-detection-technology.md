---
title: 'From R-CNN to Faster R-CNN: The Evolution of Object Detection Technology'
layout: page
comments: true
social-share: true
show-avatar: true
---

The goal of object detection is to find the location of an object in a given picture accurately and mark the object with the appropriate category. To be precise, the problem that object detection seeks to solve involves determining where the object is, and what it is.

However, solving this problem is not easy. Unlike the human eye, a computer processes images in two dimensions. Furthermore, the size of the object, its orientation in the space, its attitude, and its location in the image can all vary greatly.

From the task of image recognition, let's consider an image task. In this task, we need to identify the object in the figure and use a box to indicate its location.

![Object_detection](/object_detection.png){:class="img-responsive"}

Technically, the above task involves image recognition and positioning.

**Image recognition (classification)**

*  Input: image
*  Output: the type of object
*  Method of evaluation: accuracy

**Positioning**

*  Input: image
*  Output: the location of the box in the image (x, y, w, h)
* Method of evaluation: evaluation function intersection-over-union (IOU)

The infamous Convolutional Neural Network (CNN) technology has helped us to complete the task of image recognition. However, we still need to add some additional functions to complete the task of positioning; this is where deep-learning comes into play.

In this article, we will discuss the evolution of object detection technology from the perspective of object positioning. Here's how we can briefly denote the evolution of object detection technology: R-CNN -> SppNET -> Fast R-CNN -> Faster R-CNN.

Before we begin, let us take a closer look at Region-based Convolutional Neural Networks (R-CNN).

**Approaching Positioning as a Matter of Regression**

If we look at this as a matter of regression, then we need to predict the values of the four parameters (x,y,w,h) to get the position of the box.

![Positioning](/positioning.png){:class="img-responsive"}

**Step 1**
* Solve the simplest problem first; use a neural network to identify images.
* Fine-tune on AlexNet VGG GoogleLenet.

![Convolution](/convolution.png){:class="img-responsive"}

**Step 2**
* At the tail of the above neural network (that is, before CNN remains unchanged, we make improvements to the end of the CNN; add two headers: "Category Header" and "Regressor Header").
* Turn it into a classification + regression model.

![Class_regression](/class_regression.png){:class="img-responsive"}

**Step 3**
* Apply regression using Euclidean distance loss.
* Use SGD training

**Step 4**
* Combine the two headers in the prediction phase.
* Complete various functions.

Now we need to perform two fine-tuning operations. We can perform the first round on ALexNet, while in the second operation, we will convert the head to a regression head. The front remains unchanged, and we will just have to fine-tune it.

**Where to add the regression **

There are two available methods:

* Add it after the last convolutional layer (e.g. VGG).
* Add it after the last fully connected layer (e.g. R-CNN).

Performing the regression is quite difficult, so we need to find a way to turn this into a matter of classification. The time to merge training parameters is much longer for regression, so the network above uses a classification network to calculate the link weights of different parts of the network.

**Obtaining the Image Window**