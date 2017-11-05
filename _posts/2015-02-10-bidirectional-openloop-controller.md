---
layout: post
Title: Designing A Bi-Directional Open-Loop Position Controller
subtitle: ECE 3412 - Classic Control Systems
categories: TempleU
tags: [matlab, simulink, arduino, hardware, programming, signal, stepper,  motor, control]
bigimg: /img/posts/3412_controls/bidirectional_openloop_position-controller.png
---

# Problem
MatLab is a versatile toolbox that allows us to build digital control systems
quickly. In this lab we will use an open loop system for the control of a
stepper motor. We create the hypothetical situation of using a photo resistor
to sense the ambient light in a room. If the light is too low then we tell the
motor to open the blinds, and if the light is too high then we close the
blinds. The stepper motor is crucial for this operation in order to precisely
control the position of the blinds.  MatLab has built in functionality to use
stepper motors via an Arduino board. The stepper block has three inputs so we
can control the speed, direction, and step count directly. Using switching,
sum, difference, memory blocks we can construct our open loop control system
that controls the inputs to our stepper motor.

[Click here for full report.](
http://files.tdevin.com/blog/20150210_trejo_devin_lab02.pdf)
