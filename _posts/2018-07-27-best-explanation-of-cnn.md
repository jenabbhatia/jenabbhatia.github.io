---
title: Best Explanation of CNN
layout: page
comments: true
social-share: true
show-avatar: true
---

I came up with a very good explanation of Convlutional Neural network. 

CNNs have wide applications in image and video recognition, recommender systems and natural language processing. In this article, the example that I will take is related to Computer Vision. However, the basic concept remains the same and can be applied to any other use-case!

CNNs, like neural networks, are made up of neurons with learnable weights and biases. Each neuron receives several inputs, takes a weighted sum over them, pass it through an activation function and responds with an output. The whole network has a loss function and all the tips and tricks that we developed for neural networks still apply on CNNs. Pretty straightforward, right?

So, how are Convolutional Neural Networks different than Neural Networks?

**CNNs operate over Volumes !**

What do we mean by this?

![Convolution](/convolution_img.png){:class="img-responsive"}

Unlike neural networks, where the input is a vector, here the input is a multi-channeled image (3 channeled in this case).
There are other differences that we will talk about in a while.
Before we go any deeper, let us first understand what convolution means.

**Convolution**
![Convolution_filter](/conv_filter.png){:class="img-responsive"}

We take the 5*5*3 filter and slide it over the complete image and along the way take the dot product between the filter and chunks of the input image. For every dot product taken, the result is a scalar.

So, what happens when we convolve the complete image with the filter?

![Complete_Convolution](/complete_conv.png){:class="img-responsive"}

**Now, back to CNNs**

The convolution layer is the main building block of a convolutional neural network. The convolution layer comprises of a set of independent filters (6 in the example shown). Each filter is independently convolved with the image and we end up with 6 feature maps of shape 28*28*1.

Suppose we have a number of convolution layers in sequence. What happens then?

![Convolution_sequence](/conv_sequence.png){:class="img-responsive"}.

All these filters are initialized randomly and become our parameters which will be learned by the network subsequently.
I will show you an example of a trained network.

![Trained_network](/trained_network.png){:class="img-responsive"}.

Take a look at the filters in the very first layer (these are our 5*5*3 filters). Through back propagation, they have tuned themselves to become blobs of coloured pieces and edges. As we go deeper to other convolution layers, the filters are doing dot products to the input of the previous convolution layers. So, they are taking the smaller coloured pieces or edges and making larger pieces out of them.

Take a look at image 4 and imagine the 28*28*1 grid as a grid of 28*28 neurons. For a particular feature map (the output received on convolving the image with a particular filter is called a feature map), each neuron is connected only to a small chunk of the input image and all the neurons have the same connection weights. So again coming back to the differences between CNN and a neural network.

Other concepts of CNN will be explained in next post.