---
title: "Differential Mobile Robot Kinematics"
excerpt: "The ability of a robot to navigate effectively in its environment requires a proper drive kinematic equations. This project uses basic mathematical concepts like rigid-body motion to simulate a simple trajectory in MATLAB <img src='/images/500x300.png'>"
collection: portfolio
---
 <!--<img src='/images/500x300.png'>-->
### _Skills: Kinematics, trajectory generation, MATLAB_

****

Demo:
===

This project simulates a 2D differential mobile robot following a defined trajectory.

***
Overview
===

## Equation of motion

Consider a mobile robot in the world frame of reference $(X_w,Y_w)$. The robot is at position $(x,y)$ with respect to its center of mass. The robot has width of $2b$ and wheel radius of $2R_l$ and $2R_r$, left and right respectively. The angular velocity of the left and right wheels are $\dot{\phi}_l$ and $\dot{\phi}_r$ repectively. The robot's frame, linear velocity, angular postion, angular velocity of the robot about its center is given by $(X_r,Y_r)$, $v$, $\theta$, $\omega$ respectively.

The pose of the robot is denoted by $$\xi = [x, y, \theta]^T$$

$x, y, \theta$ needs to be determined in terms of $\dot{\phi}_{l,r}$.

$$\theta = \omega$$
$$\dot{x} = vcos\theta$$
$$\dot{y} = vsin\theta$$


***
Consider a Differential Robot as shown 
