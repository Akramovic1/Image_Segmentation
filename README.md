# Image_Segmentation

## Introduction
============

Image segmentation means that we can group similar pixels together and give these grouped pixels the same label. The grouping problem is a clustering problem. We used K-means and spectral clustering on the Berkeley Segmentation Benchmark.

## Dataset Preprocessing
=====================

The dataset contains two folders of images, the original images and the ground truth images which are saved in matlab file format. Each image has 5 ground truth segmentation that will be used later for evaluations. We worked on 50 images of the dataset and they are all landscape images to work on images with the same sizes. Below is a subplots of an original image and its ground truth segmentation.

## K-means Clustering
==================

In the K-means algorithm we cluster each image upon its pixels’ values. Each pixel has three values as we are dealing with images with 3-dimensions (R,G,B). We use this technique with 5 values for k : [3,5,7,9,11]. The result of the k-means is an array of the assignments for each pixel, so a pixel will have a value from the unique clusters numbers. After taking this assignments array we plotted the array as a coloured image with unique colour for each cluster. Below is a clustered image after k-means algorithm is applied.

## Evaluation Measures
===================

We evaluated the result segmentation using F-measure, Conditional Entropy for image I with M available ground-truth segmentation. For a clustering of K-clusters we reported our measures M times and the average of the M trials as well. And also we reported the average of the whole dataset.

## F-measures
----------

F-measure is an external validity indexes that combines the precision and recall concepts from information retrieval. Its values are within [0,1] and larger values indicate higher clustering quality. It is done after evaluating K-mean segmentation on the 50 image. We look for the unique clusters generated and take positions of pixels for each cluster then using these positions to get same pixels from ground truth to evaluate precision and recall on them. This is done for every image K times for different k-mean evaluation each with every M of ground truth images. Results are shown in table below.

## Conditional Entropy
-------------------

Conditional entropy is an external measure that relies on the entropy of partition T with respect to cluster Ci. The objective is to make the evaluation using this technique by getting the resulted clusters of our k-means and then get the positions of each pixel to get the value of it from the ground truth image. We then make our calculations upon these information and evaluate the clustering upon the resulted value. Below is a table containing some values for the conditional entropy.

## Authors
- **[Ahmed Akram](https://github.com/Akramovic1)**
- **[Rana Ayman](https://github.com/RanaAyman)**
- **[Mostafa Ahmed](https://github.com/MostafaAhmed660)**

_This README made with ❤️ by [Ahmed Akram](https://github.com/Akramovic1)
