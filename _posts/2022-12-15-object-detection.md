---
layout: post
title:  "Object Detection"
author: sal
categories: [ detection, CNN ]
tags: [image, face]
image: assets/images/model_cards_four_hands.jpg
description: "The model analyzed in this card detects one or more physical objects within an image, from apparel and animals to tools and vehicles, and returns a box around each object, as well as a label and description for each object."
beforetoc: "The model analyzed in this card detects one or more physical objects within an image, from apparel and animals to tools and vehicles, and returns a box around each object, as well as a label and description for each object."
toc: true
featured: false
hidden: false
---

The model analyzed in this card detects one or more physical objects within an image, from apparel and animals to tools and vehicles, and returns a box around each object, as well as a label and description for each object.

<div class="row justify-content-between">
<div class="col-md-8 pr-5">

<p class="mb-5"><img class="shadow-lg" src="{{site.baseurl}}/assets/images/obj-detection-model-description.png" alt="object-detection" /></p>

<h4>MODEL DESCRIPTION</h4>

<p><b>Input</b>: Photo(s) or video(s)</p>

<p><b>Output</b>: The model can detect 550+ different object classes. For each object detected in a photo or video, the model outputs:</p>
<ul>
 <li>Object bounding box coordinates</li>
 <li>Knowledge graph ID (“MID”)</li>
 <li>Label description</li>
 <li>Confidence score</li>
</ul>
<p>Model architecture: Single shot detector model with a Resnet 101 backbone and a feature pyramid network feature map.</p>

</div>

<div class="col-md-4">
<div class="sticky-top sticky-top-80">

<h4>PERFORMANCE</h4>

<p>Performance evaluated for specific object classes recognized by the model (e.g. shirt, muffin), and for categories of objects (e.g. apparel, food).</p>

<p>Two performance metrics are reported:</p>
<ul>
 <li>Average Precision (AP)</li>
 <li>Recall at 60% Precision</li>
</ul>

<p>Performance evaluated on two datasets distinct from the training set:</p>
<ul>
 <li>Open Images Validation set, which contains ~40k images and 600 object classes, of which the model can recognize 518.</li>
 <li>An internal Google dataset of ~5,000 images of consumer products, containing 210 object classes, all of which model can recognize.</li>
</ul>

</div>
</div>
</div>