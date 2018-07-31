---
layout: post
title: Introduction to Machine Learning
date: 2018-05-16
description: A learning reflection for the Machine Learning class at Stanford.
img: https://i.imgur.com/wfHr9m4.jpg
tags: [Blog, Machine Learning, Algorithms]
author: Gabriel Chen
---
## Abstract

This piece serves as a learning reflection for the Machine Learning class at Stanford. It will cover all the material of an introduction to Machine Learning.

## Introduction

The first part of this class serves as an introduction to the general definition of Machine Learning. This class is using Tom Mitchell’s definition, *“A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E”*, as the definition of Machine Learning.

This part also addressed two different types of Machine Learning, Supervised Learning and Unsupervised Learning.

**Supervised Learning** is the type that the algorithm is given a set of data and these data are labeled. For example, identifying whether an email is spam or not is a typical Supervised Learning method. We are given that these emails are spam and those are not as the dataset, and the algorithm is going to learn from these known data. There are also two types of Supervised Learning which are *Regression* and *Classification*. Regression is the kind of algorithm used to predict now data, and Classification is the type of algorithm used to classify the category of new data.

**Unsupervised Learning** is the type that the algorithm does not know anything about the data, which means the dataset is not labeled. For example, the google news is using an algorithm to find the pattern in many news feeds everyday without knowing which pattern it is sorting. In Unsupervised Learning, we do not know what we are finding or predicting, we only got a set of data to figure out the structure by ourselves. There are also two types of Unsupervised Learning which are *Clustering* and *Non-clustering*. Clustering is going to find the pattern in the dataset and sort them into different groups, and non-clustering does no require us to find a pattern in it but something else like the Cocktail party problem.

**Cocktail party problem algorithm**

	[W,s,v] = svd((repmat(sum(x, *x, 1), size(x, 1), 1).*x)*x’);

## Model and Cost Function

This part of class introduced the Cost Function to measure the error in linear regression. The Cost Function can be expressed as follow:

$$J(\theta_0, \theta_1) = \frac{1}{2m} \sum_{i=1}^m (\hat{y_i} - y_i)^2 = \frac{1}{2m} \sum_{i=1}^m (h_\theta(x_i) - y_i)^2$$

As in Machine Learning, we will have a training set to train the algorithm in order to have a hypothesis, and we are going to use this hypothesis to predict now data.

![training-model](https://i.imgur.com/7uipjKm.png)

The **Cost Function** is trying to measure the mean of the squares of the error between $$h_\theta(x_i)$$ and $$y_i$$, which are the predicted value and the true value. Therefore, this function is also called the *“Squared error function”* or *“Mean squared error”*. 

In the practice, we are trying to minimize the $$J(\theta_0,\theta_1)$$ to get the best prediction function, in which case, we are finding the global minimum of the function J. This part also mentioned a very useful way to visualize the J function using the *contour plot / contour figure* method. As the follow image shows, as close as we approach the center of this set of circles, the less error we are going to get.

![contour-plot](https://i.imgur.com/PaOFIYV.png)

## Parameter Learning

In this part of class, we introduced the method to minimize the result of the J function from last part, which called **Gradient Descent**. Gradient Descent can be expressed as follow, where $$\theta_j$$ is a vector representing both $$\theta_0$$ and $$\theta_1$$.

$$\theta_j := \theta_j - \alpha\frac{\partial}{\partial\theta_j}J(\theta_0,\theta_1)$$

In the process of Gradient Descent, the final result we want to get is the global minimum, and by this algorithm, we are going to take a small step every time starting from a random point, then eventually reach the global minimum of J as we desired. In the formula above, $$\alpha$$ is fixed as a *learning rate*, and the step is decreasing because the partial derivative is decreasing. When it reach the global minimum as a critical point, the derivative vanished to zero and the $$\theta_j$$ converged eventually.

![gradient-descent](https://i.imgur.com/qCUBUIV.png)

Note this algorithm may fail if we take $$\alpha$$ value too large since the derivitave may not converge to zero with too big steps. However, having a too small $$\alpha$$ can also slow the learning process down.

$$\begin{cases}
\theta_0 := \theta_0 - \alpha\frac{1}{m}\sum_{i=1}^m(h_\theta(x_i) - y_i) \\
\theta_1 := \theta_1 - \alpha\frac{1}{m}\sum_{i=1}^m((h_\theta(x_i) - y_i)x_i)
\end{cases}$$

---

Reference:

1. [Machine Learning](https://www.coursera.org/learn/machine-learning)-  Andrew Ng at Stanford University
