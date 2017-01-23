---
layout: post
title: PID Feedback Control of a DC motor using Experimental set-up | Man vs. Machine
subtitle: ECE 3412 - Classic Control Systems
categories: TempleU
tags: [matlab, simulink, arduino, hardware, programming, signal, pid, motor, control, feedback]
bigimg: /img/posts/3412_controls/pid_feedback_dc_motor_setup.png
---

# Problem
In Lab 6 we go head to head and challenge ourselves to see if we can manually
control the feedback network better than a PI controller can. In our Man vs
Machine challenge we are controlling the speed of a DC motor. Our system is
built inside MatLab’s Simulink toolbox interfacing with an Arduino.

In the previous lab assignment we introduced PID controllers which minimizing
the error of the system. P is the proportional gain, I is the integral gain,
and D is the derivative gain. A summation of all PID gains is fed back into the
motor model. In our manual control side of the lab we will have to adjust a
slider adjusting the gain being fed into the motor model. The problem with
using a human as a controller is the reaction time we have in adjusting the
gain. In a simulation of only five seconds the accuracy of the manual control
will depend on the individual. We also introduce the need to use a filter on
our output since the noise from position encoder is amplified when we take the
discrete derivative.

# Procedure
The first step of the procedure was to download the Simulink block from
blackboard.

Once the block was set up we had to find the top speed for our motor by
adjusting the slider gain and setting the normalization gain to 1. Once we
identified the top speed of our motor, we 1 normalized it by setting the
normalization gain, b, to 1/(top speed). Then we configured the low pass filter
block as follows.

Then we started the simulation and attempted to get the top speed to settle at
.5 by adjusting the slider gain.  Then we attempted to do the same thing by
using a PI controller designed in parallel.

Once the block was configured, we started testing by setting the P gain to 1
and the I gain to 0. We adjusted the P and I gains in attempting to get the
best possible output. The results are shown in the Results section of the
report.


[Click here for full report.](
http://files.tdevin.com/blog/20150324_trejo_devin_lab06.pdf)
