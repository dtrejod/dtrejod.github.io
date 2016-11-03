---
layout: post
title: Simple Statistics
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, mean, variance, statistics, speech, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/raw_speech_and_google_stock.png
---

# Problem
We want to learn the basics of what mean and variance represent for a given
dataset. In this, case we will look at an arbitrary speech signal and
Google’s stock data for the past eleven years (2616 days). First we
calculate the mean/variance/min/max/median for the entire set of data values
which we then use to compare to the mean/variance of smaller sections of
data. We explore how to interpreting the mean/variance values for smaller
window sizes allows us to see different overall characteristics. We also
learn some basics on reading in data from external files into MatLab to
utilize MatLab’s built in statistical functions.

# Approach and Results
To begin, we load our data into MatLab. To better understand what is
happening throughout the data we plot the signals.

Using MatLab’s built in function we find the min/max/mean/median/variance
for speech and Google stock data.

Comparing the speech signal to the Google data we see different
characteristics between the values. The mean value centers around zero
because we have an AC signal with zero DC offset. Therefore, we expect the 
mean of the signal to be zero. Variance is higher for the speech signal
because of radically changing sine wave amplitudes that compose the speech
signal. The Google stock price does not have a mean of zero since their
stock price does not oscillate around zero like the speech signal. Instead,
the Google stock mean shows the average price of the stock over the past
eleven years. Recalling that the variance is the standard deviation of a
set of data squared, we can take the square root of our variance to see a
standard deviation of 127 points. Comparing the standard deviation with the
mean we see that most of our data falls between one standard deviation
from the mean. Now we will investigate what the mean/variance of the data
looks like when we break them up into varying window/frame sizes. First we 
focus on the speech signal. We break the speech frame sizes of 40, 60,
169 and window sizes of 160 and 240.

[Click here for full report.](
http://files.tdevin.com/blog/20150120_trejo_devin_ca1.pdf)
