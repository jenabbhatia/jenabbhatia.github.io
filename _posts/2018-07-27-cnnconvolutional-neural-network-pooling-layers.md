---
title: CNN(Convolutional neural network) Pooling Layers
layout: page
comments: true
social-share: true
show-avatar: true
---

Continuing the "best explanation of CNN" post.

**Pooling Layers**

A pooling layer is another building block of a CNN.

![Pooling](/pooling.png){:class="img-responsive"}

Its function is to progressively reduce the spatial size of the representation to reduce the amount of parameters and computation in the network. Pooling layer operates on each feature map independently.

The most common approach used in pooling is max pooling.

![Max_Pooling](/max_pooling.png){:class="img-responsive"}

RELU is a part of CNN. RELU is just a non linearity which is applied similar to neural networks. The FC is the fully connected layer of neurons at the end of CNN. Neurons in a fully connected layer have full connections to all activations in the previous layer, as seen in regular Neural Networks and work in a similar way.

I hope you understand the architecture of a CNN now. There are many variations to this architecture but as I mentioned before, the basic concept remains the same. In case you have any doubts/feedback, please comment.