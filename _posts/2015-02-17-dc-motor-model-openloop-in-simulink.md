---
layout: post
title: DC Motor Model For Open-Loop Control In MATLAB Simulink
subtitle: ECE 3412 - Classic Control Systems
categories: TempleU
tags: [matlab, simulink, arduino, hardware, programming, signal, motor, control]
bigimg: /img/posts/3412_controls/dc_motor_model_openloop_in_simulink.png
---

# Problem
For the next lab we experiment working with DC motors. In the previous lab we
worked with stepper motors, which operate by supplying power to one of serval
magnets surrounding the rotor.  The difference provided by the electromagnet
causes the rotor to spin in a very precise increments.  The DC motor works in
similar fashion except with the magnet is permeant (armature) and while the
commutator provide a field difference. Due to the rather simple construction of
the DC motor we can construct a model for the DC motor using an equivalent
circuit consisting of a resistor, inductor, and dynamo. By the end of the lab
we will demonstrate the accuracy of our DC motor model via Simulink.

# Procedure
To begin designing a control for this system, we must determine the current, I,
and , and model `𝑑𝜃/𝑑𝑡` the integrals of the rotational acceleration and of the
rate of change of the armature current.

[Click here for full report.](
http://files.tdevin.com/blog/20150217_trejo_devin_lab03.pdf)
