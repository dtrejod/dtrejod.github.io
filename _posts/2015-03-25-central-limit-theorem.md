---
layout: post
title: Central Limit Theorem
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, Box-Muller, distribution, statistics, speech, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/central_limit_theorem.png
---

# Problem
The central limit theorem states that no matter the underlying distribution as
long as you have a relatively uniform mean and variance the sum of the
distributions will become normal. In our experiment we will develop our own
function that creates a uniform distribution with a number of samples N
composed of a number of random variables n. By observing the actual histogram
of our function output we explore how as we increase the number of random
variables our PDF becomes more normal. We plot the actual mean, variance, and
MSE between the actual pdf and a normal fitted distribution to observe the
underlying characteristics of our output.

Activity four of the assignment tasks us with creating a new method for
creating a normal distribution of random variables using the Box-Muller
technique. To compare the two functions we develop we time and compare the
speed and accuracy of our two approaches for creating normal distributions.

# Approach and Results
To begin we use our uniform generating function to create a single uniform
distribution. The resulting plot is obviously uniform and does not fit a normal
distribution too well. A single uniform distribution had the highest mean
squared error out of all the plots (we will look at the MSE later in the
assignment). Next we increase the number of random variables (n) to ten and
observe whether we see whether we can see application of the central limit
theorem.

At ten random variables we see a pretty normal distribution from the
sum of the samples returned using our uniform generating function. We
extrapolated from our MSE plot (Figure 1) a MSE of 0.01. Also note how the
possible range of data has increased from [-1,1] to [-10, 10]. Next we will
increase the number of random variables to one hundred and observe the actual
vs normal fitted PDF.


[Click here for full report.](
http://files.tdevin.com/blog/20150325_trejo_devin_ca8.pdf)
