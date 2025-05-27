# Mobile Manipulation Capstone

This repository contains my implementation of the **Mobile Manipulation Capstone** project from the [Modern Robotics course](https://hades.mech.northwestern.edu/index.php/Mobile_Manipulation_Capstone) by Northwestern University. The capstone brings together key robotics concepts such as forward kinematics, trajectory generation, control, and more — applied to a mobile manipulator (a robot with both a mobile base and an arm).

## 🚀 Overview

In this project, a mobile manipulator is tasked with picking up a cube from an initial location and placing it at a final location, all while coordinating motion across its arm, base, and gripper.

### Key Features
- SE(3) trajectory generation for arm and base.
- Screw theory-based kinematics.
- Feedback control using feedforward + proportional-derivative (PD) terms.
- Python-based simulator using modern robotics libraries.

## 📽️ Simulation Demo

👉 *Add a GIF or link to your YouTube video/demo here.*

For example:
![Simulation Demo](path/to/demo.gif)

or

[![Watch the simulation](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)

## 🧠 Concepts Used

- SE(3) transformations and screw theory
- Trajectory generation (cubic and quintic)
- Forward and inverse kinematics
- Feedback control (PD + feedforward)
- Gripper logic and state machine control
