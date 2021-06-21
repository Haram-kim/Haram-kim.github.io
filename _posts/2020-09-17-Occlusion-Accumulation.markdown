---
title: " ICRA2020: Moving object detection for visual odometry in a dynamic environment based on occlusion accumulation "
layout: post
date: 2020-09-17 10:44
tag: 
- matlab
- moving object detection
- occlusion accumulation
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
## Abstract
  Detection of moving objects is an essential capability in dealing with dynamic environments. Most moving object detection algorithms have been designed for color images without depth. For robotic navigation where real-time RGB-D data is often readily available, utilization of the depth information would be beneficial for obstacle recognition.
 Here, we propose a simple moving object detection algorithm that uses RGB-D images. The proposed algorithm does not require estimating a background model.
Instead, it uses an occlusion model which enables us to estimate the camera pose on a background confused with moving objects that dominate the scene.
The proposed algorithm allows to separate the moving object detection and visual odometry (VO) so that an arbitrary robust VO method can be employed in a dynamic situation with a combination of moving object detection, whereas other VO algorithms for a dynamic environment are inseparable. In this paper, we use dense visual odometry (DVO) as a VO method with a bi-square regression weight. Experimental results show the segmentation accuracy and the performance improvement of DVO in the situations. We validate our algorithm in public datasets and our dataset which also publicly accessible.

### ICRA2020 presentation

<iframe width="800" height="450" src="https://www.youtube.com/embed/VVKhPwpGHVw" frameborder="0" allowfullscreen="1"> </iframe>
  
## Paper  
[ICRA2020_Occlusion_Accumulation.pdf](https://larr.snu.ac.kr/haramkim/Paper/ICRA2020_Occlusion_Accumulation.pdf)  
## Source code
[https://github.com/Haram-kim/OcclusionAccumulation](https://github.com/Haram-kim/OcclusionAccumulation)

## Sample dataset
Dataset for source code 

Please attach the dataset to source code "/matlab code/" directory.

 [Download link](https://larr.snu.ac.kr/haramkim/dataset.zip)(60.2MB)
 
## Bibtex
```
@inproceedings{kim2020moving,
  title={Moving object detection for visual odometry in a dynamic environment based on occlusion accumulation},
  author={Kim, Haram and Kim, Pyojin and Kim, H Jin},
  booktitle={2020 IEEE International Conference on Robotics and Automation (ICRA)},
  pages={8658--8664},
  year={2020},
  organization={IEEE}
}
```

