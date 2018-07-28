---
title: Weka Explorer
layout: page
comments: true
social-share: true
show-avatar: true
---

It is amazing to learn Machine learning and data mining algorithms that are used to design a model. For learning working of different algorithms i started exploring weka tool.

Here is the small example of Weka Explorer.

WEKA is a state-of-the-art facility for developing machine learning (ML) techniques and their application to real-world data
mining problems. It is a collection of machine learning algorithms for data mining tasks. The algorithms are applied directly to a dataset. WEKA implements algorithms for datapreprocessing, classification, regression, clustering, association rules; it also includes a visualization tools. The new machine learning schemes can also be developed with this package. WEKA is open source software issued under the GNU General Public License.

**This is how Weka GUI looks:**

![Weka-GUI](/2018-07-24 23_14_34-lab1_weka.pdf - Adobe Acrobat Reader DC.png){:class="img-responsive"}

**Let's start with Weka Explorer**

Explorer is an environment for exploring data. As shown below at the very top of the window, just below the title bar there is a row of tabs. Only the first tab, ‘Preprocess’, is active at the moment because there is no dataset open. The first three 4 buttons at the top of the preprocess section enable you to load data into WEKA. Data can be imported from a file in various formats: ARFF, CSV, C4.5, binary, it can also be read from a
URL or from an SQL database (using JDBC) [4]. The easiest and the most common way of getting the data into WEKA is to store it as Attribute-Relation File Format (ARFF) file.

![Weka-explorer](/2018-07-24 23_49_38-WekaExplorer.png){:class="img-responsive"}

Now, select any data set. Suppose we select iris data set. After choosing iris data set below window appears.
![Weka-dataset](/1.png){:class="img-responsive"}

In ‘Filters’ window, click on the ‘Choose’ button. This will show pull-down menu with a list of available filters. Select Supervised->Attribute -> Discretize and click on ‘Apply’ button. The filter will convert Numeric values into Nominal.

![Weka-explorer](/weka_filter.png){:class="img-responsive"}

This are the steps of the Weka explorer part. After pre-processing you can move to classify tab for classification.  Various learning schemes available in weka include decision trees and lists, instance-based classifiers, support vector machines, multi-layer perceptrons, logistic regression, and bayes’ nets. “Meta”-classifiers include bagging, boosting, stacking, error-correcting output codes, and locally weighted learning. 

In the next post we will explore Weka classify Tab.