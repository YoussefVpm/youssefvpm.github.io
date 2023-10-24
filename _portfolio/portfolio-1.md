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

$$\dot{\theta} = \omega$$

$$\dot{x} = vcos\theta$$

$$\dot{y} = vsin\theta$$

The above equation can be written in terms of rotation matrix in the  $(X_w,Y_w)$ plane denotated as shown below;

```math
\begin{bmatrix}
\dot{x}\\
\dot{y}\\
\dot{z}
\end{bmatrix}
= \begin{bmatrix}
    cos\theta & -sin\theta & 0 \\
    sin\theta & cos\theta & 0 \\
    0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
v\\
0\\
\omega
\end{bmatrix} \tag{1}
````
if the robot is said to roll without slipping
$V_A = R_r\dot{\phi_r}$, $V_B = R_l\dot{\phi_l}$

```math
V_c = V_A + \omega \times r_{C/A}, \quad
V_c = V_B + \omega \times r_{C/B}
\tag{2}
```
but $V_C = V$. adding and substracting both terms in equation (2) we obtain

```math
v = \frac{R_r}{2}\dot{\phi_r} + \frac{R_l}{2}\dot{\phi_l}, \quad
\omega = \frac{-R_r}{2b}\dot{\phi_r} + \frac{R_l}{2b}\dot{\phi_l}

```
This can further be expressed in matrix form as 

```math
\begin{bmatrix}
v\\
\omega
\end{bmatrix}
= \begin{bmatrix}
    \frac{R_r}{2} & \frac{R_l}{2} \\
    \frac{-R_r}{2b} & \frac{R_l}{2}
\end{bmatrix}
\begin{bmatrix}
\dot{\phi_r}\\
\dot{\phi_l}
\end{bmatrix} \tag{3}
```

Finally, combining equation (1) and (2) the differential forward kinematics of the mobile robot is obtained as shown in equation (4)

```math
\begin{bmatrix}
\dot{x}\\
\dot{y}\\
\dot{\theta}
\end{bmatrix}
= \begin{bmatrix}
    \frac{R_r}{2}cos\theta & \frac{R_l}{2}cos\theta \\
    \frac{-R_r}{2b}sin\theta & \frac{R_l}{2}sin\theta \\
    \frac{-R_r}{2b} & \frac{R_l}{2b}
\end{bmatrix}
\begin{bmatrix}
\dot{\phi_r}\\
\dot{\phi_l}
\end{bmatrix} \tag{4}
```


***
Consider a Differential Robot as shown 
