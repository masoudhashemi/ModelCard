---
layout: post
title:  "Object Detection"
author: sal
categories: [ detection, CNN ]
tags: [image, face]
image: assets/images/model_cards_four_hands.jpg
description: "The model analyzed in this card detects one or more physical objects within an image, from apparel and animals to tools and vehicles, and returns a box around each object, as well as a label and description for each object."
featured: false
hidden: false
---


The model analyzed in this card detects one or more physical objects within an image, from apparel and animals to tools and vehicles, and returns a box around each object, as well as a label and description for each object.

On this page, you can learn more about how the model performs on different classes of objects, and what kinds of images you should expect the model to perform well or poorly on.

![object-detection]({{ site.baseurl }}/assets/images/obj-detection-model-description.png)

## MODEL DESCRIPTION

**Input**: Photo(s) or video(s)

**Output**: The model can detect 550+ different object classes. For each object detected in a photo or video, the model outputs:

+ Object bounding box coordinates
+ Knowledge graph ID (“MID”)
+ Label description
+ Confidence score

Model architecture: Single shot detector model with a Resnet 101 backbone and a feature pyramid network feature map.

## PERFORMANCE

Performance evaluated for specific object classes recognized by the model (e.g. shirt, muffin), and for categories of objects (e.g. apparel, food).

Two performance metrics are reported:

+ Average Precision (AP)
+ Recall at 60% Precision

Performance evaluated on two datasets distinct from the training set:

+ Open Images Validation set, which contains ~40k images and 600 object classes, of which the model can recognize 518.
+ An internal Google dataset of ~5,000 images of consumer products, containing 210 object classes, all of which model can recognize.