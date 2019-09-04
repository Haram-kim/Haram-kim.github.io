---
title: "Indoor RGB-D datasets with moving objects "
layout: post
date: 2019-08-20 11:36
tag: datasets
# image: 
# headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: haram-kim
externalLink: false
---


---
# LARR Dynamic Evironments RGB-D Dataset

## File Formats
We provide the indoor RGB-D datasets from the Kinect v2 camera.
Each sequence contains the following components.

* rgb.dir
* depth.dir
* groundtruth.dir
* groundtruth mask.dir
* association.txt
* groundtruth.txt

### rgb.dir
 The directory contains color images as 640 &times 480, 8-bit in PNG format. The name of each color image represents the recorded time in the second unit.
 
### depth.dir
 The directory contains registered depth images as 640 &times 480, 16-bit in PNG format. The name of each depth images also represents the recorded time in the second unit and is synchronized with the time of color images. The value of the depth unit is the millimeter. You can use the depth images in the meter unit by divide it into 1000.
 
### groundtruth.dir
 The directory contains color images which shows manually segmented moving objects. The background is colored as a white. 

### groundtruth mask.dir
 The directory contains black and white images obtained from the segmented color images. The white color represents the moving objects. 

### association.txt
 We matched the time and the filename and stored on association file. 

### groundtruth.txt
We provide the ground-truth trajectories which are recorded by the VICON tracker. The trajectories are represented as the time, the translation xyz and the quaternion xyzw. The current version of the ground truth trajectories is represented in global coordinates. We will transform the trajectories into the orientation of the initial camera pose.



# Datasets

| sequence name | duration | length | min <br> valid depth [\%] | description |
|---------------|:--------:|:------:|:-------------------:|-------------|
| static_tree <br> [ZIP](http://icsl.snu.ac.kr/haramkim/static_tree.zip)(0.14GB)| 23.15s | 0.00m  | 90.00% | A model tree moves in front of the fixed camera |
| static_board <br> [ZIP](http://icsl.snu.ac.kr/haramkim/static_board.zip)(0.27GB)| 24.70s | 0.00m  | 90.00% | A large-sized textured board moves which could be misrecognized as the background. |
| static_man <br> [ZIP](http://larr.snu.ac.kr/haramkim/static_man.zip)(0.23GB)| 39.91s | 0.00m | 90.00% | A man moves in front of the fixed camera. |
| static_destruct <br> [ZIP](http://icsl.snu.ac.kr/haramkim/static_destruct.zip)(0.13GB)| 45.41s | 0.00m | 90.00% | A man brings a building-shaped object A building-shaped object. |
| static_construct <br> [ZIP](http://icsl.snu.ac.kr/haramkim/static_construct.zip)(0.15GB)| 32.99s | 0.00m | 90.00% | A man removes a building-shaped object. |
| dynamic_board <br> [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_board.zip)(0.58GB)| 66.60s | 10.03m | 90.00% | A man brings a building-shaped object A building-shaped object in front of the freely moving camera.     |
| dynamic_man1 <br> [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_man1.zip)(0.37GB)| 47.57s | 5.441m | 90.00% |  A man moves in front of the freely moving camera.  |
| dynamic_man2 <br> [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_man2.zip)(0.38GB)| 48.11s | 12.41m | 90.00% | A man moves in front of the freely moving camera.  |
| dynamic_toss <br> [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_toss.zip)(0.16GB)| 82.48s | 24.42m | 90.00% | Two people toss a doll to each other.  |


