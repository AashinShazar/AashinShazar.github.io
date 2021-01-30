---
layout: page
title: Capstone
permalink: /capstone/
weight: 2
---

# **Development of Sensor Fault-Tolerant Module for High-Density EMG Pattern Recognition**

### Authors: [Don Reynolds](https://www.linkedin.com/in/donvision/ "Don Reynolds") and [Aashin Shazar](https://www.linkedin.com/in/aashinshazar/ " Aashin Shazar")
### Advised By: [Dr. Xiaorong Zhang, PhD](http://www.sfsu-icelab.org/people/ "Dr. Xiaorong Zhang, PhD")

## Overview
The need to reject bad sensor data from EMG limb control systems is well-established. Sensors experiencing temporary faults lead to misclassified gestures which lowers the gesture recognition rate. Prior work by Zhang et al. rejecting faulty sensors from a low-density EMG array needs to be adapted to higher-density EMG arrays with many dozens (or hundreds) of sensors.<sup>[1](https://pubmed.ncbi.nlm.nih.gov/25888946/)</sup> 

High density EMG measurement has several advantages over low density EMG measurement.<sup>[2](https://ncbi.nlm.nih.gov/pubmed/17085302)</sup> Placing more than one electrode on a muscle allows for sensor redundancy and a view into muscle unit activity. This provides a richer set of data to generate features from, with many muscle units being activated at different times by a single muscle. High density EMG technology shows clinical promise, and it follows that EMG fault tolerant gesture recognition systems should be extended to include them.

## The Problem
The value of dense EMG sensor arrays is that they carry redundant information as larger muscles are broken down into smaller muscle units. Closely packed sensors will carry the same or similar voltage potential amplitudes with different phase, corresponding to neighboring muscle units’ activation as the larger muscle contracts. This redundancy allows for individual faulty sensors to be removed from the dense array without losing information. The separability of non-faulty sensor data enables the use of computationally efficient pattern classification schemes such as Linear Discriminant Analysis (LDA).

Signal faults such as 1) physical impacts to an EMG electrode array or 2) myoelectric sensors not contacting the skin can significantly degrade performance of machine learning classifiers generally. LDA is no exception. For example,  artifacts contained in electrode 191 of our “Contact Artifact” dataset result from a pen striking the electrode array while a gesture is held. This brings the separation of classes from orderly to non-existent. The following plots focus only on this 191st electrode to show the need to remove this faulty sensor, which is in the area of the pen strike. Each shape represents features extracted from one window.

Note that there is orderly clustering of the seven gesture classes in the first figure. This is used as training data to place the linear discriminants. Note that the second figure has no such grouping; it contains data marred by a pen tapping on the electrode grid.

![Training Data Feature Space for Electrode 191](http://ashazar.me/assets/t1.jpg)

![Contact Artifact Data Feature Space for Electrode 191](http://ashazar.me/assets/t2.jpg)
## The SFTM Benefit

To address these issues, Zhang et al. developed the Sensor Fault-Tolerance Module (SFTM) that rejects faulty electrode data using a Linear Discriminant Analysis (LDA) classifier. By removing faulty sensors from the gesture classifier’s LDA covariance matrix and means (effectively retraining the classifier on the fly), it  reduced the number of incorrect gesture classifications. A high level  flow chart is seen in figure below. <sup>[3](https://pubmed.ncbi.nlm.nih.gov/25888946/)</sup>

![High Level View of SFTM Process](http://ashazar.me/assets/SFTM.jpg)

### Contact Artifact Set

### Lifted Electrode Set