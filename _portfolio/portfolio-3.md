---
title: "3D Projectile Motion"
excerpt: "This Experimentation involves the analysis and vizualization of trajectory of a projectile motion in 3D"
collection: portfolio
---

### _Skills: MATLAB, Kinematics, trajectory generation_

****

Demo:
===

***
Projectile Model:
===
"A projectile motion is a motion where a ball is fired in the air at an angle and is allowed to moved under the force of gravity". I woke up one morning and remembered this definition from my physics teacher in secondary school. As an engineering student, I wanted to vizualize it once more using a software tool like Matlab, as these fundamental concepts never dies once you grasp it.

Goal
=== 
The goal of this experimentation was to shoot a sperical projectile (ball, stone, etc.) and control it with the help of inputs to achieve a desired location. Then the projectile flies according to the laws of physics and thus accelerated by the force of gravity to the ground.

## Inputs:
- Initial Velocity: $v_0$
- Angle from x-y plane: $\theta$
- Angle from x-axis: $\phi$
## output 
- To graphically visualise the trajectory from start to target point.

Equation of motion
===

From the diagram below, the equation of motion was evaluated in vector and each component is independent. Therefore they can be written as;
- x-direction: $m\frac{d^2}{dt^2}x(t) = 0$
- y-direction: $m\frac{d^2}{dt^2}y(t) = 0$
- z-direction: $m\frac{d^2}{dt^2}z(t) = -mg_z$

Intergrating twice the above equation yield

- $x(t) = x_0 + v_{x,0}t$
- $y(t) = y_0 + v_{y,0}t$
- $z(t) = z_0 + v_{z,0}t - \frac{1}{2}gt^2$

Once more specifying the initial positions (x_0,y_0,z_0) in order to compute the inital velocity $v_0$,

- $v_{0,x} = v_0cos(\phi)cos(\theta)$
- $v_{0,y} = v_0sin(\phi)cos(\theta)$
- $v_{0,x} = v_0sin(\theta)$

After jumping into Matlab and spending most of the time to visualise, The result was quite satisfactory. The matlab code is displayed below as follows.



