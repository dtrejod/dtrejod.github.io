---
layout: post
title: Buffer Overflow SLMail-5.5.0 Service and Gain Root Shell
subtitle: ECE 5526 - Engineering Principles of Computer Intrusion and Detection
categories: TempleU
tags: [networking, security, kali, programming, software, linux, school, server, bash, security, python]
bigimg: /img/posts/5526_engineering_principles_computer_intrusion/bufferoverlow.png
---

# Summary
Today we introduce the buffer overflow vulnerability by using a known case
in the SLMail5.5.0 application released in 2001. We discuss how an exploit
is constructed and then use Python to create a script that will overflow
the memory buffer. By the end of the experiment we demonstrate that we
have full control of the EIP register and write a unique string to showcase
how we can use the input from the POP3 login prompt to overwrite this register.

[Click here for full report.](
https://github.com/dtrejod/myece5526/blob/master/projects/20160407_slmail_rootshell_bufferoveflow/20160407_trejo_devin_slmail_bufferoverflow.pdf)
