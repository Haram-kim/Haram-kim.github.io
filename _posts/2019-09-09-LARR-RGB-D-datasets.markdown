---
title: "LARR RGB-D Dataset for Dynamic Environments"
layout: post
date: 2019-08-20 11:36
tag: 
- datasets
- moving objects
- dynamic environments
# image: 
# headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
category: project
author: haram-kim
externalLink: false
---


---
## LARR RGB-D Dataset for Dynamic Environments

### File Formats
We provide the indoor RGB-D datasets from the Kinect v2 camera.
Each sequence contains the following components.

* rgb.dir
* depth.dir
* groundtruth.dir
* groundtruth mask.dir
* association.txt
* groundtruth.txt

#### rgb.dir & depth.dir
 The rgb directory contains color images as 640 &times 480, 8-bit in PNG format and the depth directory contains registered depth images as 640 &times 480, 16-bit in PNG format. The name of each color image represents the recorded time in the second unit and is synchronized with the time of each others. The value of the depth unit is the millimeter. You can use the depth images in the meter unit by divide it into 1000.
 
 
#### groundtruth.dir & groundtruth mask.dir  
 The directory contains color images which shows manually segmented moving objects. The white color represents the background in **groundtruth.dir** and represents the moving objects in **groundtruth mask.dir**. 

#### association.txt & groundtruth.txt
 We matched the time and the filename and stored on association file. We also provide the ground-truth trajectories which are recorded by the VICON tracker. The trajectories are represented as the time, the translation xyz and the quaternion xyzw. The current version of the ground truth trajectories is represented in global coordinates. We will transform the trajectories into the orientation of the initial camera pose.

#### Inrinsic Paramter

```
fx = 544.2582548211519 # focal length x
fy = 546.0878823951958e # focal length y
cx = 326.8604521819424 # optical center x
cy = 236.1210149172594 # optical center y

# depth scale for the 16-bit image
factor = 1000

# radial distortion coefficient
k1 = 0.0369
k2 = -0.0557
```


### Datasets

| sequence name | duration | length | min <br> valid depth [%] | description |
|---------------|:--------:|:------:|:-------------------:|-------------|
| <br> **static_tree** [ZIP](http://icsl.snu.ac.kr/haramkim/static_tree.zip)(0.14GB) <br> | 23.15s | 0.00m  | 90.00% | A model tree moves in front of the fixed camera |
| <br> **static_board** [ZIP](http://icsl.snu.ac.kr/haramkim/static_board.zip)(0.27GB) <br> | 24.70s | 0.00m  | 90.00% | A large-sized textured board moves which could be misrecognized as the background. |
| <br> **static_man** [ZIP](http://larr.snu.ac.kr/haramkim/static_man.zip)(0.23GB)| 39.91s <br> | 0.00m | 90.00% | A man moves in front of the fixed camera. |
| <br> **static_destruct** [ZIP](http://icsl.snu.ac.kr/haramkim/static_destruct.zip)(0.13GB) <br> | 45.41s | 0.00m | 90.00% | A man brings a building-shaped object A building-shaped object. |
| <br> **static_construct** [ZIP](http://icsl.snu.ac.kr/haramkim/static_construct.zip)(0.15GB) <br> | 32.99s | 0.00m | 90.00% | A man removes a building-shaped object. |
| <br>**dynamic_board** [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_board.zip)(0.58GB) <br> | 66.60s | 10.03m | 90.00% | A man brings a building-shaped object A building-shaped object in front of the freely moving camera.     |
| <br> **dynamic_man1** [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_man1.zip)(0.37GB) <br> | 47.57s | 5.441m | 90.00% |  A man moves in front of the freely moving camera.  |
| <br> **dynamic_man2** [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_man2.zip)(0.38GB) <br> | 48.11s | 12.41m | 90.00% | A man moves in front of the freely moving camera.  |
| <br> **dynamic_toss** [ZIP](http://icsl.snu.ac.kr/haramkim/dynamic_toss.zip)(0.16GB) <br> | 82.48s | 24.42m | 90.00% | Two people toss a doll to each other.  |


