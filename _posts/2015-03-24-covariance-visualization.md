---
layout: post
title: Covariance Visualization
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, correlation, covariance, statistics, speech, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/covariance_visualization.png
---

# Problem
Today we introduce multivariable sample spaces. We will learn more about
covariance or how closely two sets of data are correlated. Using MatLab
we will be able to construct some random sets of data and observe the
covariance. Specifically we will utilize MatLab’s 3D visualization tool
to observe the PDFs of our random vectors. Plotting in 3D will allow us
to see the covariance and other general characteristics of our two random
variables.

First we will start with generating two random arrays which are
independently generated uniformly between zero and one. The task has us
noting the general shape and meaning behind our 3D PDF or surf plot.

Second we will tell MatLab to construct our two random variables in
accordance to four different covariance matrices (seen in Figure 2).
Using these covariances and also a mean of [6 6] for both randomly
generate variables, we are able to construct distributions which are not
all normal. To observe the covariance we create a support region or plane
which intersects the distribution as seen in Figure 1. We will see for
covariances matrices which are not the identity matrix the variances of
our random variables is not equal in all directions. Note how the diagonal
corresponds to the variance of the values and the off diagonal tells us
the correlation.

# Approach and Results
We begin with our first task of creating two randomly generated uniform
variables between 0 and 1. We can use MatLab’s random number generator
to complete the task. To find the histogram of the 2 variables we use
MatLab’s function ‘hist3’. In the previous assignment we emphasized and
proved how the number of samples you take can influence whether your data
reaches your expected output.Therefore we generate 100,000 vectors and sum
all the results so to guarantee our output produces accurate results.
Below we plot our overall histogram:

[Click here for full report.](
http://files.tdevin.com/blog/20150324_trejo_devin_ca7.pdf)
