---
title: Classification using Weka
layout: page
comments: true
social-share: true
show-avatar: true
---

In the earlier post of "Weka Explorer" we have seen how to load data into weka and data pre-processing using filter option. Let's explore the classify tab of weka.

Classifiers in WEKA are the models for predicting nominal or numeric quantities. The learning schemes available in WEKA include decision trees and lists, instance-based classifiers, support vector machines, multi-layer perceptrons, logistic regression, and bayes’ nets. “Meta”-classifiers include bagging, boosting, stacking, error-correctingoutput codes, and locally weighted learning.

Once you have your data set loaded, all the tabs are available to you. Click on the ‘Classify’ tab.

Click on ‘Choose’ button in the ‘Classifier’ box just below the tabs and select C4.5 classifier WEKA -> Classifiers -> Trees -> J48.

When training set is complete, the ‘Classifier’ output area on the right panel of ‘Classify’ window is filled with text describing the results of training and testing. A new entry appears in the ‘Result list’ box on the left panel of ‘Classify’ window.

![Weka-classify](/weka_classify.png){:class="img-responsive"}

Here you can see the accuracy of the model is  95% . This follows from the kappa statistics "0.93", which indicates the existence of moderate statistical dependence.

**Visualisation of results:**
After training a classifier, the result list adds an entry. WEKA lets you to see a graphical representation of the classification tree. Right-click on the entry in ‘Result list’ for which you would like to visualize a tree. It invokes a menu containing the following items:

![Weka-tree](/weka_tree.png){:class="img-responsive"}

WEKA also lets you to visualize classification errors. Right-click on the entry in ‘Result list’ again and select ‘Visualize classifier errors’ from the menu:

![Weka-error](/weka_classify_error.png){:class="img-responsive"}