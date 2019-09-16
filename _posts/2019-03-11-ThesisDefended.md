---
layout: posts
title: Master's Thesis Defended!
description: I succesfully defended my thesis! In my thesis I proposed and tested various ways to learn target concepts in imprecisely labeled data. This type of algorithm is known as Multiple Instance Learning. The multiple target concept learning algorithm proposed maximizes target detection rather than just target endmember estimation and is shown on simulated hyperspectral dataset as well as a challenging airborne collected hyperspectral dataset.
tags: blog
header:
  teaser: assets/images/ThesisGulfportRGB.jpg
---

Over the course of my studies at the University of Florida, I developed algorithms for subsurface explosive hazard detection. A large problem with developing algorithms on this data is the innate data ambiguity and imprecision. Due to this, a multiple instance learning method was investigated, where learning is done using groups of labeled data instead of singly labeled data points. The proposed algorithm learns multiple target concepts to perform target detection. The sections below highlight my thesis which strictly contains hyperspectral data results due to subsurface explosive hazard data restrictions.

<p align="center">
	<img src="/assets/images/ThesisGulfportRGB.jpg" width="400" height ="400" />
</p>

## Motivation

## Single Target Algorithm

The Multiple Instance Adpative Cosine Estimator and Spectral Match Filter (MI-ACE and MI-SMF) learns a single target signature that maximizes the following objective function.

<p align="center">
	<img src="/assets/images/MIACEObjFun.PNG"/> 
</p>

This algorithm assumes the data follows the multiple instance learning framework, where the data has been labeled into two types of groups or bags, positive and negative. A positive bag is defined as a group of data points where at least one of the data points, also known as instances, is an item of interest, known as a target instance(s). A negative bag is defined as a group of data points where all of the data points are pure background, known as non-target instances.

## Proposed Algorithms

The Multi-target Multiple Instance Adaptive Cosine Estimator and Spectral Matched Filter (Multi-target MI-ACE and Multi-target MI-SMF) algorithm learns a dictionary of target concepts to perform target detection by maximizing the following objective function.

<p align="center">
	<img src="/assets/images/ThesisObjFun.PNG"/> 
</p>

Throughout my studies, many variations were designed and tested. These variations are listed and briefly described below.

### Greedy Approach

### Clustering Approaches

### Weighted Approaches

### Uniqueness Term

---

## Details

Learning Multiple Target Concepts from Uncertain, Ambiguous Data Using the Adaptive Cosine Estimator and Spectral Match Filter

---

## Future Work

---

## Thesis github

The thesis PDF can be found [here](https://github.com/GatorSense/Publications/blob/master/Bocinsky2019Thesis.pdf "Lab publications repository").

The source code is located on the Machine Learning and Sensing Lab's [github repository](https://github.com/GatorSense/Multi-Target-MI-ACE_SMF "Multi-target MI-ACE/SMF repository").

Thanks,  
James

---
