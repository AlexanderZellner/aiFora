# aiFora

## Introduction

This repository implements different fairness algorithms initally shown by the aif360 project[1]. It uses different data sets and different approaches to display potential biases in dataset. It is largly inspired by [IBM](http://aif360.mybluemix.net/check). Generally speaking there are three possibilities to correct a bias in a dataset pre, inter, and post. The majority of the approaches used in this repository focus on the preprocessing step as it looked most promising.

Further in order to achieve a better understanding I highly recommend the [aif360](https://github.com/Trusted-AI/AIF360) repository. Especially the guides and tutorials offered: https://github.com/Trusted-AI/AIF360/tree/master/examples. Most of the following code is inspired by these.

## Contents

* [notebooks](https://github.com/AlexanderZellner/aiFora/tree/main/notebooks)
    * **adult**
    Contains two different notebooks varying in their protected attribute. Both use the aif360 classifier metric.
    * **compas** 
    Contains **3 different notebooks** relevant for fairness:
        - lr_classifier: Classifier metric with linear regression classifier
        - lr_pipeline: Simple pipeline for a linear regression model
        - sklearn_classifier: Instead of using custom aif360 functions this approach uses standarized methods (pandas) to improve the handling and processing of the fairness data.
    * **credit score**
    Contains three notebooks of which two differ in their protected attribute. Whereas, *sexclassifier.ipynb* and *sexbinary.ipynb* vary in their classifier approach.
* [aif360-Fork](https://github.com/AlexanderZellner/AIF360). I would advise to check the commit messages for further insides. I added some simple helper functions to improve procedures.

## Tipps and Helpful links

* The documentation of [aif360](https://aif360.readthedocs.io/en/latest/modules/generated/aif360.metrics.ClassificationMetric.html) provides great detail about what is possible.
* At the beginning using the binary approach might be easier, but it is limited in functionality. Thus, I recommend using a proper classifier.
* I was not able to produce the exact same results as IBM, but the results of the compas notebooks came very close.
* The original [paper](https://arxiv.org/pdf/1810.01943.pdf) from IBM


[1] Bellamy, R. K., Dey, K., Hind, M., Hoffman, S. C., Houde, S., Kannan, K., ... & Zhang, Y. (2018). AI Fairness 360: An extensible toolkit for detecting, understanding, and mitigating unwanted algorithmic bias. arXiv preprint arXiv:1810.01943.
