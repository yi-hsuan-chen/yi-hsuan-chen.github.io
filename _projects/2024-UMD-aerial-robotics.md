---
title: "Fast-Planner Implementation, and Multiple AprilTags Detection and Navigation"
collection: projects
type: "Graduate Course Project"
venue: "University of Maryland, ENAE788M-Hands on Aerial Robotics"
date: 2024-05-02
location: "College Park, USA"
---

This project aims to detect AprilTag positions and use a planner to generate the drone's trajectory. We use multiple AprilTags to provide waypoints for the drone, leveraging the tracking camera's video feed for detection. The Fast-Planner is used to plan a safe, kinodynamically feasible trajectory based on these waypoints. The flight tests were done with a Modal AI VOXL2 drone at UMD Brin Family Aerial Robotics Lab. <br /><br /> ![](http://yi-hsuan-chen.github.io/files/fast_planner_gazebosim.gif) 

Advisor: [Dr. Joseph Conroy](http://www.avl.umd.edu/people/joseph-conroy.html)
Team Members: [Piyush Goenka](https://github.com/piyush-g0enka), [Yi-Hsuan Chen](https://yi-hsuan-chen.github.io/)  
[[Download Technical Report here]](http://yi-hsuan-chen.github.io/files/ENAE788M_final_project_team1_piyush_yihsuan.pdf)

## Visual Detection - Multiple AprilTags Detection
- Use tracking camera's video feed for AprilTag detection
- Transform detected poses from camera frame to drone's body frame and inertial frame
- Generate waypoints based on detected AprilTag positions
- Monitor drone position and publish next waypoint when within 0.2m of current waypoint

### Real Drone Implementation 
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/SFHdX0v_6u8?si=VeBQG6Ok7DkAJqMg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

## Path Planning - Fast-Planner Implementation
- Integrate Fast-Planner (ROS1) with PX4 and Gazebo (ROS2) using ros1_bridge package
- Use kinodynamic path searching and B-spline optimization for trajectory generation
- Transform coordinate frames between ENU (Fast-Planner) and NED (PX4)
- Implement data transmission between ROS1 and ROS2 using custom Python scripts
<p align="center">
    <img src="http://yi-hsuan-chen.github.io/files/simu_framework.png" width="510">
</p>
<p align="center">
    <img src="http://yi-hsuan-chen.github.io/files/fast_planner.png" width="510">
</p>

### Gazebo Simulation
- Successfully demonstrated waypoint tracking using Fast-Planner
- Drone hit 10 waypoints consecutively with smooth trajectories
- Validated the ROS1-ROS2 bridge implementation
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/rnxRFLKCjiU?si=L8rS7KR2kMs02iPu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

### Real Drone Attempt
- Achieved basic waypoint following but faced challenges with:
  - Vehicle odometry accuracy
  - Data transmission delays through ROS1 bridge
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/uLpx8BnWYbk?si=LrM_PZ_ePIflX1jg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

## References
\[1\] Boyu Zhou, Shaojie Shen, and Fei Gao. "A robust and efficient trajectory planner for quadrotors", 2020. [(link)](https://github.com/HKUST-Aerial-Robotics/Fast-Planner)  
\[2\] Nilaos. "ROS 2 package that provides bidirectional communication between ROS 1 and ROS 2", 2023. [(link)](https://github.com/ros2/ros1_bridge)  
\[3\] Benjamin Perseghetti. "Integration between ROS (1 and 2) and Gazebo simulation", 2019. [(link)](https://github.com/gazebosim/ros_gz)  