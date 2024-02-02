---
title: "NMPC-based control for Quadrotor trajectory tracking with constrained inputs"
collection: teaching
type: "Graduate Course Projects (EE 372)"
# permalink: /teaching/2014-spring-teaching-1
venue: "King Abdullah University of Science and Technology (KAUST)"
date: 2021-05-03
location: "Thuwal, Saudi Arabia"
---

Advisor: [Dr. Meriem Laleg](https://scholar.google.com/citations?user=oyKikokAAAAJ&hl=en) <br />This work aims to develop a nonlinear model predictive controller to achieve trajectory tracking for a quadrotor subject to input constraints.  
<p align="center">
<iframe width="400" height="200" src="https://www.youtube.com/embed/jzHL5VHJmtA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>


## Motivation
The objective is to find a control strategy that allows the states of a quadrotor to converge to an arbitrary set of time-varying reference states. Though it is possible to control a quadrotor using linear control techniques by linearizing the system around a trim point even if the quadrotor model is coupled and highly nonlinear, nonlinear control methods are preferred to obtain better performance. Multiple nonlinear methods such as sliding mode, backstepping, adaptive and feedback linearization have been demonstrated to be effective for quadrotor control.  

However, none of these control methods take state and control constraints into account, we might face instability issues due to saturation and violation of feasible region. Hence, the nonlinear MPC is proposed to control the quadrotor and handle input constraints at the same time. Also, less effort for tuning is required in MPC structure, since we can simply put weights on states based on the degree of importance. The main drawback of MPC is the computation complexity, because the optimization problem need to be solved iteratively over a whole time period. Thanks to the development of technology, more powerful solvers are available to cope with MPC’s computation
demand.

## Methodology
In this study, a nonlinear MPC controller is developed to achieve trajectory tracking for a quadrotor subject to input constraints. The optimal control problem (OCP)
is transformed into a nonlinear programming problem (NLP) using multiple shooting method, which requires less computational effort and provides higher numerical
stability. The IPOPT solver of the open-source optimal tool CasADi is used to solve the nonlinear programming problem in an efficient way. Multiple flight scenarios
were performed to show the NMPC address the control problem in high performance.  

[Github link](https://github.com/yi-hsuan-chen/Nonlinear-Model-Predictive-Control)

## Simulation Results
The figure shows that NMPC has the ability to stabilize the quadrotor on the desired trajectory, and to keep the control inputs in the operation range over a whole time interval simultaneously. In other words, the nonlinear MPC can achieve satisfactory performance and handle constraints, which would be more practicable compared to conventional control methods.  
<p align="center">
<img src="https://raw.githubusercontent.com/yi-hsuan-chen/yi-hsuan-chen.github.io/master/fig/helix_u.png" width="510">
</p>

However, the closed-loop of the quadrotor was not guranteed in every desired trajectories. The stability issue involves the initial condition, selection of terminal constraints and length of prediction horizon. Therefore, more systematic stability analysis should be furthered investigated to improve reliability.

## Oral Presentation
<p align="center">
<iframe width="680" height="400" src="https://www.youtube.com/embed/CHVspeZNykM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

## References
\[1\] Luukkonen, T., “Modelling and control of quadcopter”, Independent research. project in applied mathematics, Espoo (2011) [(link)](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/viewer.html?pdfurl=https%3A%2F%2Fwww.mecharithm.com%2Fwp-content%2Fuploads%2F2020%2F11%2Fquadrotor_dynamics.pdf&clen=1316755&chunk=true)  
\[2\] Gijs van Lookeren Campagne. A nonlinear model predictive control based evasive manoeuvre assist function.  
\[3\] K. Worthmann, M. W. Mehrez, M. Zanon, G. K. I. Mann, R. G. Gosine, and M. Diehl. Model predictive control of nonholonomic mobile robots without
stabilizing constraints and costs. IEEE Transactions on Control Systems Technology, 24(4):1394–1406, 2016. [(link)](10.1109/TCST.2015.2488589)  
\[4\] MPC and MHE implementation in Matlab using Casadi Workshop hosted by [Mohamed W. Mehrez](https://www.youtube.com/watch?v=RrnkPrcpyEA&t=2s)

<!-- The objective is to design a flight control algorithm for a quadrotor and study further how to recover control in the presence of single rotor loss. The error transformation and reconfiguration techniques combined with sacrificing yaw control are applied to realize fault-tolerant control under actuator failures. The input saturation is not considered in our case. This project is mainly hosted by Prof. Chao-Chung Peng, the director of Intelligence Embedded Control Laboratory (IEC-Lab) in Department of Aeronautics and Astronautics, National Cheng Kung University, Taiwan. It was also a part of collaboration with the Industrial Technology Research Institute, a technology research and development institute in Taiwan.

## Related Publication
Lien, Y.-H.; Peng, C.-C.; Chen, Y.-H. Adaptive Observer-Based Fault Detection and Fault-Tolerant Control of Quadrotors under Rotor Failure Conditions. Appl. Sci. 2020, 10, 3503. [[Paper Link]](https://doi.org/10.3390/app10103503)

## Conclusion
From the above video, we can find that the quadrotor is able to track desired trajectory when fault-tolerance control is engaged. The yaw control is sacrificed to maintain the controllability of x, y, and z directions. In this project, I was mainly charge of testing flight simulator, collecting data, and presenting our research results to collaborators every week. -->