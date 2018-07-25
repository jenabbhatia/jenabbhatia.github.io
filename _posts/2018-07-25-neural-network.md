---
title: Neural Network
layout: page
comments: true
social-share: true
show-avatar: true
---

Neural networks are limitations of how our brain works. They've had a big recent resurgence because of advances in computer hardware. There is evidence that the brain uses only one "learning algorithm" for all its different functions. Scientists have tried cutting (in an animal brain) the connection between the ears and the auditory cortex and rewiring the optical nerve with the auditory cortex to find that the auditory cortex literally learns to see. 

Neural networks are used to solve complex non-linear hypothesis. Let's examine how we will represent a hypothesis function using neural networks. At a very simple level, neurons are basically computational units that take input (dendrites) as electrical input (called "spikes") that are channeled to outputs (axons).

Neural network  model looks like:
![Neural_net](/Network331.png){:class="img-responsive"}


In our model, our dendrites are like the input features x_1..........x_n, and the output is the result of our hypothesis function:

In this model our x0 input node is sometimes called the "bias unit." It is always equal to 1.

In neural networks, we use the same logistic function as in classification . In neural networks however we sometimes call it a sigmoid (logistic) activation function.

Our "theta" parameters are sometimes instead called "weights" in the neural networks model.

Visually, a simplistic representation looks like:

![Neural_net_rep](/neural_net_representation.png){:class="img-responsive"}
Our input nodes (layer 1) go into another node (layer 2), and are output as the hypothesis function.

The first layer is called the "input layer" and the final layer the "output layer," which gives the final value computed on the hypothesis.

We can have intermediate layers of nodes between the input and output layers called the "hidden layer."

We label these intermediate or "hidden" layer nodes and call them "activation units."

![Activation_Unit](/activation_unit.png){:class="img-responsive"}

If we had one hidden layer, it would look visually something like:

![hidden_layer](/hidden_layer.png){:class="img-responsive"}

The values for each of the "activation" nodes is obtained as follows:

![activation_values](/activation_values.png){:class="img-responsive"}

This is saying that we compute our activation nodes by using a 3×4 matrix of parameters. We apply each row of the parameters to our inputs to obtain the value for one activation node. Our hypothesis output is the logistic function applied to the sum of the values of our activation nodes, which have been multiplied by yet another parameter matrix Theta^2
containing the weights for our second layer of nodes.

Each layer gets its own matrix of weights, Θ ^(j).

The dimensions of these matrices of weights is determined as follows:

If network has sj units in layer j and s j+1 units in layer j+1, then Θ ^(j)  will be of dimension ![theta_formula](/thehta_formulae.png){:class="img-responsive"}.

The +1 comes from the addition in Θ^(j) of the "bias nodes," x_0 and Θ^(j). In other words the output nodes will not include the bias nodes while the inputs will.

Example: layer 1 has 2 input nodes and layer 2 has 4 activation nodes. Dimension of Θ ^(1)  is going to be 4×3 where sj=2 and s_{j+1} = 4s, so  ![theta_formula](/thehta_formulae.png){:class="img-responsive"} = 4 * 3.