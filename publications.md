---
layout: page
title: Publications
url: publications
---

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

# Generator Assisted Mixture of Experts For Feature Acquisition in Batch
*Vedang Asgaonkar, Aditya Jain, Abir De*
<br>
AAAI-24 accept, [arxiv](https://arxiv.org/pdf/2312.12574.pdf)
<br>
We deal with a feature acquisition task for classification. Primarily, we are given an initial subset of features, which is used to decide a new subset of features to be queried. Unlike prior work, this is done in a batch setting, new features are queried simultaneously instead of sequentially. This implies that the new features to be queried can only be conditioned on the set of initial features. Subsequently, we perform classification based on the availble feature values. We propose GENEX, an algorithm for deciding which subset of features to query under a budget constraint on the number of features that can be queried.

## Salient Features
* We propose a greedy algorithm to decide the set of features to be acquired on the training set
* We utilize Locality Sensitive Hashing to enable quick retrieval of the optimal feature subset during inference
* We construct a mixture of experts model to perform the classification task on a heterogenous domain of feature subsets
* We utilize a generator to produce a subset of the features that are to be acquired. This reduces the number of queries that need to be performed to the oracle set of features.
* We provide theoretical backing and experimental verification to our greedy algorithm

## Problem Setup
We use $$x \in \boldsymbol{R}^n$$ to denote a feature vector and $$y$$ to denote the classification label.