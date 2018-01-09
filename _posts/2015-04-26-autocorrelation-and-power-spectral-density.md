---
layout: post
title: Autocorrelation and Power Spectral Density
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, autocorrelation, power spectral density, gaussian, noise, psd, pdf, distribution, statistics, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/autocorrelation_and_power_spectral_density.png
---

# Problem
Today we look over autocorrelation and power spectral density (PSD) again.
Unlike in our last analysis, we now will compare and contrast the
autocorrelation and PSD of several different signals.

The first signal we will observe is a Gaussian noise signal that contains two
hundred samples. For the autocorrelation plot we will generate one with 20 lags
in it. Since our signal is a noise signal we expected that its power across all
frequencies to be constant.

The second signal is a single impulse with one hundred samples in it. The lags
in our autocorrelation will range up to 20. In similar vein to the Gaussian we
expected a flat frequency response since our time domain signal is short in
time. Short in time means broad in frequency.

The third signal is also an impulse signal that repeats every 20 samples. Since
we have a train of impulses we increase the number of samples to 200 and the
number of lags to 60. The PSD should be similar to the single impulse.

The fourth signal generated is a sinewave whose periods occurs every 20
samples. The frequency of said sine wave is dependent on the sample frequency.
Up to know we have used a sample frequency of 8KHz therefore our sinewave has
as frequency of fs/T=8kHz/20=400Hz. We repeat our analysis of the
autocorrelation and PSD as explained before. Also for this sine wave case we
analyze the behavior if we were to change the number of samples between 14, 17,
20, 23, and 26.

The sixth signal is a sine-wave with a noise component. Given a SNR of 10db we
perform the same analyses.

# Approach and Results
The Gaussian white noise is expected to have energy across all frequencies. We
can find the autocorrelation function of our white noise and observe how just
by chance the signal looks to be correlated a bit. In truth we know the signal
is entirely random.

In our second signal we have an impulse. Recall from Signal and systems that
short in the time domain correlates to wide in the frequency domain. If we find
the autocorrelation of our signal we will note that the signal is never
correlated to itself since it is not periodic. Our power spectral density thus
is flat like our Gaussian white noise signal.


[Click here for full report.](
http://files.tdevin.com/blog/20150426_trejo_devin_ca11.pdf)
