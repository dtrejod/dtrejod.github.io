---
layout: post
title: Analytic Approach To Determining Closedloop Gain For A Second Order DC Motor System
subtitle: ECE 3412 - Classic Control Systems
categories: TempleU
tags: [matlab, simulink, arduino, hardware, programming, signal, pid, root locus, control, motor, feedback]
bigimg: /img/posts/3412_controls/determining_closedloop_gain_second_order_dc_system.png
---

# Problem
Previously we have only experimented with implementing PID controllers into our
systems, but sometimes we want to adjust the amount of correction in of PID
controllers. A feedback system with proportional gain can easy adjustment to
PID controllers without having to adjust the PID itself. Adjusting the
proportional gain allows us to change the percent overshoot, and settling time
of a system’s response.

In this lab we will analyze the technique designers use to find to system
responses. The lab confronts us using Routh-Hurwitz table to find the poles of
a system. From the poles we apply our equations to find percent over shoot
`(%OS)`, and settling time `(Ts)`. Also we incorporate Microelectronic circuit
analysis to construct our PID controller using discrete analog components.

# Procedure
The first step of the experiment required us to load raw data from the
blackboard into the workspace. The data was very noisy, so we filtered it using
a tenth order median filter. This filtered data was then passed to the System
Identification Toolbox, where we estimated a second order transfer function. We
then applied a proportionality gain controller to the system, and solved for
the value of k that would result in a 10% overshoot. Once we found the new k,
found the step response of the new transfer function (the transfer function
with the controller applied). Once we had the step response, we validated that
we did in fact get a 10% overshoot. We also plotted the root locus diagram and
validated found the k value that would make the system critically damped.  Once
this was completed, we repeated the process for a third order transfer function
of the same filtered data. We redid all calculations, and analyzed an overshoot
of 150%, and what happens when the proportionality constant grows too large.

[Click here for full report.](
http://files.tdevin.com/blog/20150331_trejo_devin_lab07.pdf)
