---
title: Face Recognition using Image Similarity
layout: page
comments: true
social-share: true
show-avatar: true
---

Hello all,
     In earlier post i have discussed face recognition using pre-configured docker image for face recognition. In this post i am presenting face recognition using Image similarity.
		 
There are three most common techniques used for image similarity
		 
1.  Comparing Histograms:  One of the simplest and fastest method. Proposed, decades ago to find image similarities. The idea is that a forest will have lot of green, and human face will have a lot of pink or other features. So, if you compare two pictures with forests, you will get some similarity between hostograms, because you have lot of green in both.
				Disadvantage: Its too simplistic.
				Opencv method : compareHist().

2. Template Matching: A good example is [matchTemplate](https://stackoverflow.com/questions/8520882/matchtemplate-finding-good-match).  It convolves hte search image with the one being searched into. It is usually used to find smalled image parts in a bigger one.
				Dis-advantage: It only returns good results with identical images, same size & orientation.
				OpenCV method: matchTemplate()

3. Feature Matcing : Consider one of the most efficient ways to do image search. A number of features are extracted from an image, in a way that gurantees that the same features will be recognized again, even it is rotated/scaled/skewed. The features extracted this way can be matched against other image feature sets. Another image that has a high proportion of the features in the first one is most probably depicting the same object/scene. It can be used to find the relative difference in shooting angle between pics, or the amount of overlapping.
				Dis-advantage: It may be slow. It is not perfect.