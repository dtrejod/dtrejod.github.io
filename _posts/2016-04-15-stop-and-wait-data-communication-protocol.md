---
layout: post
title: Stop and Wait Data Communication Protocol
subtitle: ECE 4532 - Data Communications
categories: TempleU
tags: [programming, c code, networking, microcontroller, flowcontrol, TCP]
bigimg: /img/posts/4532_data_comm/linear_block_code_parity.png
---

# Summary
Today we introduce the stop-and-wait sliding window transmission method 
and compare the performance for difference values of window size and 
sequence size. We find that a window size that is too small decreases 
performance but having a window size that is too big introduces the 
probability that errors will occur during transmission. From testing 
multiple parameters we find that a windows size of 04 produces the results
with the fastest transmission for our 26 packet long test message.

[Click here for full report.](
https://github.com/dtrejod/myece4532/blob/master/lab5/trejo_devin_005.pdf)
