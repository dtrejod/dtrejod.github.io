---
layout: post
title: NMAP Network Footprint and A Recon on Metasploitable
subtitle: ECE 5526 - Engineering Principles of Computer Intrusion and Detection
categories: TempleU
tags: [programming, software, linux, school, server, bash, security, python]
bigimg: /img/posts/reacon-metasploitable/virtualmachine-env.png
published: true
date: 2016-02-29
---

Today, we look more in depth into NMAP, a popular open-source security 
scanner. We are interested in analyzing the accuracy of NMAP, as well as 
the network footprint seen when using some of its more popular scripts. 
To begin we create a network of six Virtual-Box machines which consist of 
three Metasploitable Linux, one Kali Linux, one Ubuntu 14.04, and one 
Centos 7 machines. We find the banner information gathered from a NMAP 
scan to be accurate if a machine’s security is not properly configured. 
Using Wireshark we analyze the amount of packets sent during a full version 
scan to be 182 KB over 123.54 seconds or 1.47 KB/sec. Next we use a Python 
program to exploit the Simple Mail Transfer Protocol (SMTP) to gather a 
list of known users on a server. We have success in validity emails on our 
Metasploitable virtual machine.

[Click here for full report](files.tdevin.com/blog/20160227_trejo_devin_002.pdf)