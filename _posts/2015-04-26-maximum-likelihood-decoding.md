---
layout: post
title: Maximum Likelihood Decoding
subtitle: ECE 3522 - Stochastic Processes in Signals and Systems
categories: TempleU
tags: [random, mean, histogram, pdf, distribution, statistics, speech, software, matlab, programming]
bigimg: /img/posts/3522_stochastic_systems/maximum_likelihood_decoding.png
---

# Problem
The assignment we will explore today is to create a simulation that will allow
us to apply a pattern recognition system based around maximum likelihood
classification. The entire process is a simulation thus we will be required to
first generate our own Gaussian distrusted data, then transform it using
principle component analysis as we explored in CA12, and lastly classify it. In
our assignment we will focus on analyzing five different cases. In each case we
will only change our sigma2 parameter. The parameters we analyze our laid out
below:

`Class 1: μ1=[1; 1] ; C1=[1 0;0 1]
`Class 2: μ2=[−1; −1] ;C2=[sigma2 0.5; 0.5 sigma2] sigma2→0.25,0.5,1.0,2.0,4.0`

As can be seen our first class parameter does not change. It is a Gaussian
distributed multivariate array with equal energy in all directions. It has a
mean that centers around [1,1]. Our second class energy changes but the
correlation between our multivariate array stays constant at 0.5 Our second
class will be center around [-1, -1].

From classification we use maximum likelihood classification. Before performing
the classification we transform each set of data using principal component
analysis. The process will convert our data sets so our data is not
independently correlated. Thus our covariance matrix will have an off diagonal
of zeros. By performing the transformation we can perform a Euclidean distance
calculation (instead of a Mahalanobis distance) to the means of our data sets.
What we wish to see is how the energy of our data correlates to the
classification success of our data.

# Approach and Results
We begin our analysis by create multiple cases to compare. The results are laid
out below. We plotted both the original un-transformed data (left) with the
transformed scatter plot of our classes (right).

The above case is our first test. We see our two sets of data and how the
principal component analysis transforms our data so that they become
uncorrelated. Our transformation process is performed to the expected means of
data sets where we see there is hardly any difference for our first set of
data. For our second class our mean differs slightly. The error can be produced
in our data creation process. We still see that even though we our mean is off
by 23% our classification error rate is low for this case.

[Click here for full report.](
http://files.tdevin.com/blog/20150426_trejo_devin_ca13.pdf)
