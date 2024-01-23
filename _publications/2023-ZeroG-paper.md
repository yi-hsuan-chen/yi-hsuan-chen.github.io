---
title: "Adaptive Observer-Based Fault Detection and Fault-Tolerant Control of Quadrotors under Rotor Failure Conditions"
collection: publications
permalink: /publication/2020-FTC-paper
excerpt: 'The objective is to design a flight control algorithm for a quadrotor and study further how to recover control in the presence of single rotor loss. The error transformation and reconfiguration techniques combined with sacrificing yaw control are applied to realize fault-tolerant control under actuator failures. The input saturation is not considered in our case.'
date: 2020-05-19
venue: 'Applied Science'
paperurl: 'https://www.mdpi.com/2076-3417/10/10/3503'
citation: 'Lien, Y. H., Peng, C. C., & **Chen, Y. H. (2020)**. Adaptive observer-based fault detection and fault-tolerant control of quadrotors under rotor failure conditions. Applied Sciences, 10(10), 3503.'
---
This paper aims to propose a strategy for the flight control of quad-rotors under single
rotor failure conditions. The proposed control strategy consists of two stages—fault detection (FD)
and fault tolerant control (FTC). A dual observer-based strategy for FD and fault estimation is
developed. With the combination of the results from both observers, the decision making in whether
a fault actually happened or the observed anomaly was caused by an external disturbance could be
distinguished. Following the FD result, a control strategy for normal flight, as well as the abnormal
one, is presented. The FTC considers a real-time coordinate transformation scheme to manipulate
the target angles for the quad-rotor to follow a prescribed trajectory. When a rotor fault happens,
it is going to be detected by the dual observers and then the FTC is activated to stabilize the system
such that the trajectory following task can still be fulfilled. Furthermore, in order to achieve robust
flight in the presence of external wind perturbation, the sliding mode control (SMC) theory is further
integrated. Simulations illustrate the effectiveness and feasibility of the proposed method.

[[Download paper here]](http://yi-hsuan-chen.github.io/files/applsci-10-03503-v2.pdf)

<!-- Recommended citation: Lien, Y. H., Peng, C. C., & **Chen, Y. H.** (2020). Adaptive observer-based fault detection and fault-tolerant control of quadrotors under rotor failure conditions. Applied Sciences, 10(10), 3503. -->