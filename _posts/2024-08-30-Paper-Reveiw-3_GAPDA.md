---
layout: post
title:  "[Paper Review] Gradient Alignment based Partial Domain Adaptation (GAPDA) using a domain knowledge filter for fault diagnosis of bearing"
author: sal
categories: [Paper Review]
image: assets/images/GAPDA_FRONT.jpg
---
> The third paper I will review is 'Gradient Alignment based Partial Domain Adaptation (GAPDA) using a domain knowledge filter for fault diagnosis of bearing' written by Ph.D. candidate Yong Chae Kim from [SNU HAI Lab][SNU-HAI-LAB].

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

![15]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/15.png)

![16]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/16.png)

![17]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/17.png)

![18]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/18.png)

![19]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/19.png)

## 4. Validation Studies

![21]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/21.png)

![22]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/22.png)

![23]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/23.png)

![24]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/24.png)

![26]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/26.png)

![27]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/27.png)

![29]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/29.png)

![31]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/31.png)

![34]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/34.png)

![35]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/35.png)

![37]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/37.png)

![40]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/40.png)

![42]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/42.png)

## 5. Discussion

![47]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/47.png)

![48]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/48.png)

![49]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/49.png)

![50]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/50.png)

## 6. Conclusion

![52]({{ site.baseurl }}/assets/images/PaperReview_GAPDA/52.png)


[SNU-HAI-LAB]: https://hai.snu.ac.kr