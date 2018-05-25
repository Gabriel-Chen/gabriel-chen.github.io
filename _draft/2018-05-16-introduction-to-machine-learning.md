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

This piece serves as a learning reflection for the Machine Learning class at Stanford. It will cover all the material about an introduction to Machine Learning.

## Introduction

The first part of this class serves as an introduction to the general definition of Machine Learning. This class is using Tom Mitchell’s definition, *“A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E”*, as the definition of Machine Learning.

This part also addressed two different types of Machine Learning, Supervised Learning and Unsupervised Learning.

**Supervised Learning** is the type that the algorithm is given a set of data and these data are labeled. For example, identifying whether an email is spam or not is a typical Supervised Learning method. We are given that these emails are spam and those are not as the dataset, and the algorithm is going to learn from these known data. There are also two types of Supervised Learning which are *Regression* and *Classification*. Regression is the kind of algorithm used to predict now data, and Classification is the type of algorithm used to classify the category of new data.

**Unsupervised Learning** is the type that the algorithm does not know anything about the data, which means the dataset is not labeled. For example, the google news is using an algorithm to find the pattern in many news feeds everyday without knowing which pattern it is sorting. In Unsupervised Learning, we do not know what we are finding or predicting, we only got a set of data to figure out the structure by ourselves. There are also two types of Unsupervised Learning which are *Clustering* and *Non-clustering*. Clustering is going to find the pattern in the dataset and sort them into different groups, and non-clustering does no require us to find a pattern in it but something else like the Cocktail party problem.

Cocktail party problem algorithm

{% highlight octave %}
[W,s,v] = svd((repmat(sum(x, *x, 1), size(x, 1), 1).*x)*x’);
{% endhighlight %}

## Model and Cost Function


---

Reference:

1. [Machine Learning](https://www.coursera.org/learn/machine-learning)-  Andrew Ng at Stanford University
