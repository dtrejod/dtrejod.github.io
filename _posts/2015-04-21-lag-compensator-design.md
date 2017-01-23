---
layout: post
title: Lag Compensator Design
subtitle: ECE 3412 - Classic Control Systems
categories: TempleU
tags: [matlab, simulink, arduino, hardware, programming, signal, motor, transfer function, root locus, pid]
bigimg: /img/posts/3412_controls/lag_compensator_design.png
---

# Problem
In this lab we will be experiment with lead compensator design. This is
important because lead compensators add poles and zeros to the closed loop
transfer function, which in turn alters the shape of the root locus. If we can
alter the shape of the root locus, we can ensure that the poles that give us
our desired settling time and steady state error lie on the root locus, which
leaves us to simply calculate the proportional gain that gives us the desired
pole.

# Procedure
To begin the design of a lead compensator we need to analyze our DC motor
system. We build our traditional DC motor apparatus and measure the system
response to a 0.5 unit step. Also as before we can estimate our first order
transfer function for the data collected using the system identity toolbox
built into MatLab. After we have our transfer function we can plot the root
locus fairly easily also in Matlab using the `rlocus` function. The transient
response of the will show lots of steady state error.
`𝐾𝑃 = lim 𝐺(𝑠) 𝑠→0 → 𝑒𝑠𝑠 = 𝑅/(1 + 𝐾𝑃)`

Now that we have the steady state error we can try to reduce the error by
introducing a lead compensator. We pick a new steady state error of 0.25 and
find the lead compensator accordingly for when our zeros of our compensator are
0.01, 0.1, and 1. The compensator will change our transfer function so that our
new transfer function becomes: `𝐶𝐺(𝑠) = 𝐶𝐿𝑒𝑎𝑑(𝑠) ∗ 𝐺(𝑠)`

For each lead compensator case we plot the root locus and the corresponding
transient response. We compare each compensator to determine which produces
the best response.

[Click here for full report.](
http://files.tdevin.com/blog/20150421_trejo_devin_lab09.pdf)
