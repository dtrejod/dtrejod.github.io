---
layout: post
title: Two Dimension Parity Checking
subtitle: ECE 4532 - Data Communications
categories: TempleU
tags: [programming, c code, networking, microprocessor]
bigimg: /img/posts/4532_data_comm/two_dimension_parity.png
---

# Summary
Lab 3 introduces two-dimensional parity error checking for an original 30 
byte transmission between a client computer and a PIC32 server. The 
two-dimensional parity checking code allows us to encode our original 
message with redundant bits to detect errors in a received message. The 
original message is arranged in a grid and the parity bit is calculated 
across the rows and down the columns. Our original 30 byte string increases
in size to a 35 byte string that contains the parity information. We 
demonstrate that our two-dimensional decoder is capable of detecting and 
correcting one bit errors from the client received message.


[Click here for full report.](
http://files.tdevin.com/blog/20160311_trejo_devin_003.pdf)
