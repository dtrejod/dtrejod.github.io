---
layout: post
title: TCP/IP Buffer Transmission
subtitle: ECE 4532 - Data Communications
categories: TempleU
tags: [programming, c code, networking, microprocessor]
bigimg: https://github.com/dtrejod/myece4532/raw/master/lab1/images/client_server_frame_analysis.png
---

# Summary
In the TCP/IP Buffered Data Transmission lab we look into sending a large
message across several smaller datagrams. Blocking data up into smaller 
sizes is commonly done on the server side when a client requests a large 
message to be sent across the network. In this experiment we use our PIC32 
MCU to provide a 1060 byte message and parse it in smaller blocks of data. 
We then send each block of data to the client and analyze the transmission
in Wireshark to see if the server does send the data successfully and if 
the client receives the intended full message. We show success in 
transmission between server and client when our larger message is parsed 
into two and three separate datagrams with arbitrary delays put in between. 
The delays are put in to simulate transmission propagation time. Upon 
trying to send our larger message in 50 byte blocks we receive server 
re-transmission behavior that is expected when using TCP as a transfer 
protocol, as discuss in the previous lab.

[Click here for full report.](
http://files.tdevin.com/blog/20160227_trejo_devin_002.pdf)
