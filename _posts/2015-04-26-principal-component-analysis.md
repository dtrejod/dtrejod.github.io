---
layout: post
title: Principal Component Analysis
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, correlation, eigen values,  distribution, statistics, speech, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/principle_component_analysis.png
---

# Problem
In this assignment we introduce Principal Component Analysis which will allow
us to take a set of data and transform it so appears uncorrelated. Using some
data built into MatLab we can successfully apply principal component analysis
in a study that tracks 349 different cities’ climate, housing, health, crime,
transportation, education, arts, recreation, and economics statuses.

To begin applying principal component analysis we first must find our whitening
transform matrix. The transform matrix is constructed from the Eigen vectors
and values of our data’s covariance matrix.

The transformed data will appear uncorrelated. A test we perform to see if this
is true is to compute the covariance matrix of our transformed data. If the
data is truly uncorrelated the off-diagonal will be all zeros.

Lastly we will want to see which two cities are the most closely related. We
will apply a Euclidean distance to determine which ratings of two cities are
the most closely related. We perform this step for our un-transformed,
transformed, and first three criteria.

# Approach and Results
From the Eigen value matrix we see that the largest value occurs in the 9th
column which tells us that the 9th column has the most variance in it. You can
see this is true if you reference Figure 1. Referencing the corresponding
categories matrix loaded in with the cities data we see how the 9th column
corresponds to the economic status of each city. Since this Eigen value is the
largest we know the Eigen vector corresponding to this Eigen value has the most
weight in the transform. The second largest Eigen Value occurs in the 8th
column which correspond to a city’s recreation. If we remove the two rating
criteria with the largest Eigen values we will observe how much weight they
have on the variance of the ratings data set (climate, housing, health).

[Click here for full report.](
http://files.tdevin.com/blog/20150426_trejo_devin_ca12.pdf)
