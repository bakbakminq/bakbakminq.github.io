---
layout: post
title:  "[Prior Knowledge] About Bearings"
author: sal
categories: [Paper Review]
image: assets/images/PaperReview_Revolution and peak discrepancy-based domain alignment method for bearing fault diagnosis under very low-speed conditions/VLS.jpg
---
> The papers that I cover are all about bearings. So we need prior knowledge about bearings to fully understand.

## 1. Introduction

**Why Bearing Fault Diagnosis is Essential**

Bearings are essential components of rotating machinery. Bearing failure can result in the complete shutdown of a system, thereby making the diagnosis of bearings critical for maintaining the safety and reliability of machinery systems. Numerous researches have developed various algorithms by adopting signal-processing techniques for diagnosis of mechanical systems, including bearings.

**Previous Research and Limitations**

* *Unsupervised Domain Adaptation (UDA)* <br> : Reduces the distribution discrepancy between a source domain and a differently distributed target domain in an unsupervised manner, thereby improving the accuracy of the prediction in the target domain

* *Domain Adversarial Neural Network (DANN)* <br> : Minimize the distribution differences between source and target domains in image data with domain discriminator

* *Deep Convolutional Transfer Learning Network (DCTLN)* <br> : Operates by reducing the statistical distribution difference between the two domains in high-dimensional data spaces

\> Limitation <br>
They assume that each label in the source and target data is of equal quantity, which implies identical label distribution. However, in industrial settings, the occurrence of faults is often less frequent than the occurrence of normal conditions, leading to a data imbalance problem

* *Class-Imbalance Adversarial Transfer Learning (CIATL)* <br> : Both marginal and conditional distribution adaptation to train class-separate diagnostic knowledge

* *Partial Adversarial Domain Adaptation (PADA)* <br> : Assigning class weights to the task classification loss and domain classification loss based on the predicted values for the target data

* *Stacked-auto-encoder based Partial Adversarial Domain Adaptation* <br> : Employs stacked auto-encoders and a weighted classifier to address the fault diagnosis problem in PDA scenarios for rotating machinery

\> Limitation <br> In adversarial learning, which performs both task classification and domain classification, it is challenging to guarantee initial task classification performance, making successful domain adaptation difficult

## 2. Preliminary

**\- Domain Adaptation (DA)**

* In machine systems, the distribution of training and testing data can diverge due to differences in the operating conditions under which the data was collected, or due to component variations <br >→ Leads to domain shift

* While many industrial sites have a substantial amount of unlabeled data, utilizing unlabeled data for supervised learning presents challenges

**→** This issue can be addressed by UDA

**\- Partial Domain Adaptation (PDA)**

Extracting domain-invariant features in scenarios where the target domain has fewer labels compared to the abundant label set of the source domain

**\- Partial adversarial Domain Adaptation (PADA)**

Before we discuss PADA, let's see DANN first. DANN is one of the representative methods of UDA.
Feature extractor 𝐺_𝑓 : takes an image or signal as input and produces a high-dimensional latent space as output
Predictor 𝐺_𝑝 : classifies labels based on the high-dimensional latent space
Domain discriminator 𝐺_𝑑 : classifies the domain
Operates effectively when the number of labels in the source and target are consistent, and their distributions are identical
If the number of labels in the target is fewer than that of the source labels, negative transfer can occur


## 3. Proposed Method

![14]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/14.png)




[SNU-HAI-LAB]: https://hai.snu.ac.kr