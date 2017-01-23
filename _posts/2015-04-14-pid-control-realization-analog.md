---
layout: post
Title: PID Control Realization Using Analog Components
subtitle: ECE 3412 - Classic Control Systems
categories: TempleU
tags: [matlab, simulink, arduino, hardware, programming, signal, motor, control, feedback, circuit, analog, pid]
bigimg: /img/posts/3412_controls/pid_control_realization_analog.png
---

# Problem
In this lab we will be working with an analog PI controller. This is important
for understanding of this course because everything up to this point was done
in hardware, MatLab was doing a lot behind the scenes that we were unaware of.
This was part of the reason we were seeing such noisy outputs in previous lab.
The noise came from the fact that the Arduino was getting interrupted while
attempting to send commands. This resulted in the count that translated into
the speed of the motor to be too high, which caused the noise. To avoid this,
we had to build an analog circuit that would free up the Arduino to communicate
without being interrupted. It was also important to view what an actual PI
controller looked like in hardware. This method is also more robust. If we look
at Figure 1, shown below, we can see how we can achieve the proportional and
integral gains using analog components. We also note that a change in the value
of the components changes the value of the gains.

# Procedure
The majority of the lab is spent building the Microelectronic circuit that will
allow us to avoid using the Arduino as the control and data collector.

There are three major circuit parts for this circuit. The first thing we take
notice of is the frequency to voltage converter circuit (F-V). The encoder
which is attached to the motor shaft records speed into different pulse widths.
The challenge is to convert this PWM signal into a voltage reference we could
use to record the speed of the motor.

After we have a voltage reference that tells us the speed of our motor we are
able to compare this voltage to a reference point set by a potentiometer. We
perform this by using a difference amplifier.  This amplifier is equivalent to
the difference node (see Figure 4) in the block diagram we seen in previous
labs which produces our error signal.

Now that we have our difference or error signal we can use a PID controller to
feed into the motor.  The equivalent circuits for this PID controller in an
Op-Amp is seen in Figure 2. In this lab we will change the values of the
capacitance and resistors to change our P, I and D gains.

The lab focuses on coming up with an understanding of how this analog circuit
compares to the digital equivalent we made in previous labs.


[Click here for full report.](
http://files.tdevin.com/blog/20150414_trejo_devin_lab08.pdf)
