---
layout: post
title: Signal to Noise Ratio and Filtering
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, noise, autocorrelation, fourier transform, statistics, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/signal_to_noise_ratio_and_filtering.png
---

# Problem
Chapter 10 of Fundamentals of Applied Probability and Random Processes by
Oliver-C-Ibe introduces applied concepts for stochastic processes. A stochastic
process is one where the output contains a component of randomness.  In this
assignment we combine knowledge from Signals and Systems with Stochastic
Systems and observe what trends we can conclude.  To begin we will create a
function that will provide us a sine wave with a component of noise. In the
previous assignment we demonstrated how we could create a function using the
Box-Muller technique to create an array of normally distributed variables. We
now use that function to create a Gaussian noise aspect and combine it with our
signal. The amount of noise we combine with our sine wave is dependent on the
signal to noise ratio. We can define the SNR as follows:

In our function we will be able to take in the desired output frequency in
hertz, the length (in seconds), the sample frequency, and SNR.

Now that we are capable of creating a signal with noise we observe the
relationship of the autocorrelation to the SNR. Autocorrelation tells us how
correlated a signal is to itself at different shift values (τ). In our case we
will take the first 16 shifts of a 500Hz sine wave sampled at 8000Hz.
Inspecting the autocorrelation at different shifts will tells us at SNR does
our noise impact our sine wave considerably. Also at these various SNRs we
inspect the Fourier transform of the signal. We are curious to observe what
noise looks like in the frequency domain.

Lastly, we explore the idea of the power spectral density function. The PSD is
the Fourier transform of the autocorrelation function and tells us the power at
certain frequencies of our signal. To demonstrate the concept we create a
signal with 30db SNR. Passing the signal through a digital filter shown below
provides us with a clearer output. We find the PSD and plot the Fourier
transform of our filtered signal squared. We expect the resulting plots should
be equal.

`y[n]=0.5y[n-1]+x[n]`

# Approach and Results
To begin we create a function that produces a sine wave with noise given a
certain SNR. Using the Box-Muller method allows us to quickly create an array
of normal variables, but we still need to find the variance of the noise.
Recall that the variance also equals the power of a signal. Using equation 1 we
can find the power of the noise. Then we can feed it into our normal number
generator to create a noise signal. We create a table of the power in the
entire signal given different SNR.


[Click here for full report.](
http://files.tdevin.com/blog/20150401_trejo_devin_ca9.pdf)
