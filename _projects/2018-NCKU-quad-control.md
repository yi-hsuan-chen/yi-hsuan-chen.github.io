---
title: "Fault Tolerant Control of a quadrotor under actuator failures"
collection: projects
type: "Undergraduate Research"
venue: "National Cheng Kung University (NCKU), Intelligent Embedded Control (IEC) Lab, Department of Aeronautics and Astronautics"
date: 2018-01-15
location: "Tainan, Taiwan"
---
The objective is to design a flight control algorithm for a quadrotor and study further how to recover control in the presence of single rotor loss. <br /><br /> ![](http://yi-hsuan-chen.github.io/files/ftc_drone.gif) 

Advisor: [Dr. Chao-Chung Peng](https://scholar.google.com/citations?user=YzN8zoUAAAAJ&hl=en)<br />

## Motivation
Quadrotors have been widely used in many fields, such as agriculture, cargo delivery, surveillance, aerial photography, military fields and environmental monitoring. Therefore, the safety of people under the flying area is now a concerned and an important issue. To ensure the safety of flight of the quad-rotor and the safety of people under or nearby the flying area, it is necessary to adopt an appropriate field safety strategy, such as **fault-tolerant control**, when a quad-rotor is malfunctioning.

## Methodology
In the study, we aim to design a flight controller to stabilize a drone when one of its rotor fails. During the loss of a single rotor, the applied torque can no longer achieve ordinary orientation control. This specific scenario could be regarded as a reduced attitude stabilization problem. Since there is no control effort imposed on the yaw dynamics,
there would be an unexpected yaw motion such that incorrect control torque vector may be induced. Thus, the flight controller in this paper consists of two parts — a coordinate transformation based outer-loop controller and an inner-loop stabilization controller. Note that the yaw angle obtained from measurement must be applied as a coordinate transformation to get the desired angles such that the torque can be correctly re-distributed when one rotor fails. The more details can be found in the related publication below.
<br /> <br /> ![](http://yi-hsuan-chen.github.io/files/ftc.jpg)

## Related Publication
Lien, Y.-H.; Peng, C.-C.; Chen, Y.-H. Adaptive Observer-Based Fault Detection and Fault-Tolerant Control of Quadrotors under Rotor Failure Conditions. Appl. Sci. 2020, 10, 3503. [[Paper Link]](http://yi-hsuan-chen.github.io/files/ftc.jpg)

## Simulation Results
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/kR5VIGB4Mvk?si=eNvbgKRFEW2LjbeG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>




<!-- ## Methodology
The error transformation and reconfiguration techniques combined with sacrificing yaw control are applied to realize fault-tolerant control under actuator failures. The input saturation is not considered in our case. This project is mainly hosted by Prof. Chao-Chung Peng, the director of Intelligence Embedded Control Laboratory (IEC-Lab) in Department of Aeronautics and Astronautics, National Cheng Kung University, Taiwan. It was also a part of collaboration with the Industrial Technology Research Institute, a technology research and development institute in Taiwan.

## Methodology
From the above video, we can find that the quadrotor is able to track desired trajectory when fault-tolerance control is engaged. The yaw control is sacrificed to maintain the controllability of x, y, and z directions. In this project, I was mainly charge of testing flight simulator, collecting data, and presenting our research results to collaborators every week.


## Youtube Video -->

<!-- ---
title: "Teaching experience 2"
collection: teaching
type: "Workshop"
permalink: /teaching/2015-spring-teaching-1
venue: "University 1, Department"
date: 2015-01-01
location: "City, Country"
---

This is a description of a teaching experience. You can use markdown like any other post.

Heading 1
======

Heading 2
======

Heading 3
====== -->
