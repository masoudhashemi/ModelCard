---
layout: post
title:  "Face Detection"
author: john
categories: [ detection, CNN ]
tags: [red, yellow]
image: assets/images/model_cards_audience_profiles.jpg
description: "The model analyzed in this card detects one or more faces within an image or a video frame, and returns a box around each face along with the location of the faces' major landmarks. The model's goal is exclusively to identify the existence and location of faces in an image. It does not attempt to discover identities or demographics."
featured: false
hidden: false
---


The model analyzed in this card detects one or more faces within an image or a video frame, and returns a box around each face along with the location of the faces' major landmarks. The model's goal is exclusively to identify the existence and location of faces in an image. It does not attempt to discover identities or demographics.

On this page, you can learn more about how well the model performs on images with different characteristics, including face demographics, and what kinds of images you should expect the model to perform well or poorly on.

## MODEL DESCRIPTION

![walking]({{ site.baseurl }}/assets/images/model-info-img.png)

**Input**: Photo(s) or video(s)

**Output**: For each face detected in a photo or video, the model outputs:

+ Bounding box coordinates
+ Facial landmarks (up to 34 per face)
+ Facial orientation (roll, pan, and tilt angles)
+ Detection and landmarking confidence scores.
+ No identity or demographic information is detected.

Model architecture: MobileNet CNN fine-tuned for face detection with a single shot multibox detector.

## PERFORMANCE

Overall model performance, and performance sliced by different image and face characteristics, were assessed, including:

+ Derived characteristics (face size, facial orientation, and occlusion)
+  Face demographics (human-perceived gender presentation, age, and skin tone)

Overall performance measured with Precision-Recall (PR) values and Area Under the PR Curve (PR-AUC) - standard metrics for evaluating computer vision classifiers. Download raw performance results data here.

Disaggregated performance measured with Recall, which captures how often the model misses faces with specific characteristics. Equal recall across subgroups corresponds to the “Equality of Opportunity”fairness criterion.

Performance evaluated on: Three research benchmarks distinct from the training set:

+ A subset of Open Images
+ Face Detection Data Set and Benchmark
+ Labeled Faces in the Wild
