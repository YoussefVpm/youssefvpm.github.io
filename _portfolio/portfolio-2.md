---
title: "Unicycle Kinematic Simulation"
excerpt: "simulation of different scenarios of a Kinematics Car-Like robot in simulink using different controllers"
collection: portfolio
---

### _Skills: MATLAB, Simulink, Kinematics, trajectory generation_

****

Demo:
===

This project simulates a 2D Kinematics of a Unicycle Mobile robot using simulink. It uses different controller gains based on different scenarios to make the mobile robot achieve specific task.

Overview
===

- The robot changes maneuver in a simple lane
- The robot moves from an arbitary point to a defined position in space
- The robot follows a spcified line by steering.

***

## Kinematics Equation

Consider the Unicycle robot in a 2D world frame as shown in the figure. The generalized coordinates of the vehicle's configuration is $q = (x, y, \theta)$ 

The kinematic model of the vehicle can be expressed as 

$$\dot{x} = vcos\theta$$

$$\dot{y} = vsin\theta$$

$$\dot{\theta} = \frac{v}{L}tan\gamma$$

where;

- $\theta$ = orientation angle of robot
- $\gamma$ = steering angle
- $L$ = length of wheel base
- $v$ = linear velocity of robot
- $\dot{\theta}$ = angular velocity
- $\ddot{x}$, $\ddot{y}$ are linear acceleration in $x$ and $y$ directions respectively

