---
title: GPU's becoming the new CPU, in the Era of Artificial Intelligence
layout: page
comments: true
social-share: true
show-avatar: true
---

Traditionally, computing power is associated with the number of CPUs and the cores per processing unit.  During 90's, application performance and database throughput were directly proportional to the number of CPUs and availble RAM. While these factors are critical to achieve desired performance of enterprise appications, a new processor started to gain attention - **Graphics Processing Unit (GPU)**.

But, why is the GPU getting so much attention now? The answer lies in the rise of deep learning, an advanced machine learning technique that is heavily used in AI and Cognitive Computing. Deep learning powers many scenarios including autonomous cars, cancer diagnosis, computer vision, speech recognition and many other intelligent use cases.

Like most of the ML algorithms, deep learning relies on sophisticated mathematical and statistical computations. Artificial Neural Networks (ANN), Convolutional Neural Networks (CNN) and Recurrent Neural Networks (RNN) are some of the modern implementations of deep learning. These neural nets emulate human brain with close resemblance to neuroscience. Each type of neural net is aligned with a complex use case like classification, clustering and prediction. For example, image recognition and face recognition use CNN while Natural Language Processing (NLP) relies on RNN. ANN, the simpler ones of all the neural networks is often used predictions involving numerical data.

Irrespective of the type of neural network used, all the deep learning algorithms perform complex statistical computations. From typical stock market data to the picture of a cat to the radiology report, everything is first decoded into a set of numbers. In the case of images, the first step is to turn them into the grayscale format and then to assign a number to each pixel depending on how light or dark it is. As we can imagine, a simple selfie shot from a mobile phone translates to few million pixels, which in turn translates to a large matrix of numbers. During the training phase of deep learning, these matrices of numbers are fed as input into the neural network along with the correct classification. For example, by training the neural network with 1000s of cat images, we are going to get a model that can easily recognize a cat visible in a photo. This training process is all about correlating multiple pixels (numbers) to find patterns of a cat image. The correlation involves multiplying millions of matrices with each other to arrive at the right result. To increase the training speed, these operations need to be done in parallel.

Typical CPUs are designed to tackle calculations in a sequential order, which means each mathematical operation will have to wait for the previous to complete. A CPU with multiple cores may marginally speed up the calculation by offloading the operations to each core. But, as we know CPUs with multiple cores are prohibitively expensive, making them less optimal for training neural networks.

Enter GPU, and we have a processor with thousands of cores capable of performing millions of mathematical operations in parallel. There is a similarity between graphic rendering and deep learning. Both these scenarios deal with a huge number of matrix multiplication operations per second. That’s one of the reasons why laptops or desktops with high-end GPUs are preferred for deep learning. Nvidia has a programming model for GPU called CUDA that lets developers build parallel programs.

To put things in perspective, Nvidia’s latest GPUs come with 3,584 cores while Intel’s top end server CPUs may have a maximum of 28 cores.

The growth of GPU has brought Nvidia into the limelight. While the traditional PC and server market is witnessing a decline, the GPU market is getting hot. Top public cloud providers including Amazon, Google, IBM and Microsoft offer GPU-based VMs in the cloud. These virtual machines are powered by the latest Nvidia Tesla processors, which deliver the required performance for training deep learning models. Cloud customers are taking advantage of the pay-by-hour pricing model to access these specialized machines on demand.

Google, one of the pioneers in AI and deep learning has announced Tensor Processing Unit or TPU – a chip that is designed to perform complex math operations with massive parallelism. A version of TPU called Cloud TPU is available for customers using Google’s IaaS offering, Google Compute Engine.

Artificial Intelligence and Machine Learning are changing the landscape of enterprise IT. The recent interest in GPUs is squarely attributed to the rise in AI and ML.