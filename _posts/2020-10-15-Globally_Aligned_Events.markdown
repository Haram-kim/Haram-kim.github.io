---
title: " RA-L2021: Real-time rotatinoal motion estimation with contrast maximization over globally aligned events "
layout: post
date: 2021-06-10 10:00
tag: 
- event camera
- rotational motion estimation
- contrast maximization
- globally aligned event
- real-time

# image: 
# headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
category: project
author: haram-kim
externalLink: false
---


---


<img src="http://larr.snu.ac.kr/haramkim/SNU_LARR.png" alt="SNU LARR logo" width = "600">

## Abstract
Contrast maximization is an event camera application that can estimate angular velocity, depth, and optical-flow using a subset of events observed in a temporal window. In the estimation of rotational motion, we can compute the angular position by integrating the angular velocity. However, the accumulation of drift error degrades the accuracy of motion estimation. If the contrast maximization framework utilizes events measured before the temporal window, the performance of the framework will be improved, including the alleviation of drift error in motion estimation.
In this work, we utilize the globally aligned event data and propose the rotational position and velocity estimation method using an event camera only. The proposed algorithm not only maximizes contrast of an image of events in a single temporal window but also maximizes the contrast image of events observed over time. Our algorithm works in real-time by reducing additional computations of the existing contrast maximization. We confirm the real-time operation with a single-core CPU on a laptop and show that the maximum error is within 3 degrees on public data sets and acquired real-world data sets.
To contribute to the community, we provide the source code and the real-world data sets to the public.

### Video

<iframe width="800" height="450" src="https://www.youtube.com/embed/wHeyIWEuEg4" frameborder="0" allowfullscreen="1"> </iframe>

### Source code
[https://github.com/Haram-kim/Globally_Aligned_Events](https://github.com/Haram-kim/Globally_Aligned_Events)

## Datasets

### Data sets with VICON ground truth pose

| sequence name | description |
|:-------------:|-------------|
| <br> **360_indoor** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/360_indoor.zip)(29.4MB) <br> | 360_indoor |
| <br> **fast_motion** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/fast_motion.zip)(23.7MB) <br> | fast_motion |
| <br> **ESIM_panorama** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/ESIM_panorama.zip)(30.5MB) <br> | ESIM_panorama |
| <br> **ESIM_OpenGL** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/ESIM_OpenGL.zip)(36.3MB) <br> | ESIM_OpenGL |

### Data sets without ground truth pose

| sequence name | description |
|:-------------:|-------------|
| <br> **360_outdoor** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/360_indoor.zip)(74.9MB) <br> | 360_indoor |
| <br> **fast_roll** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/fast_roll.zip)(25.1MB) <br> |fast_roll |
| <br> **lobby** <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/lobby.zip)(35.7MB) <br> | lobby |
| <br> **rooftop**  <br> [ZIP](https://larr.snu.ac.kr/haramkim/event_dataset/rooftop.zip)(49.2MB) <br> | rooftop |

