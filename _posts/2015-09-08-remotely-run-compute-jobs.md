---
layout: post
title: Remotely Run Compute Jobs
subtitle: ECE 3822 - Software Tools for Engineers
categories: TempleU
tags: [softwaretools, software, bash, linux, Server, Programming, big data, Temple, SuperComputer]
bigimg: /img/posts/3822_software_tools/bash-run-remotely.png
---

# Problem
The purpose of this assignment is to demonstrate how to run jobs on a 
remote machine. Running jobs remotely is useful when running long, 
intensive computing scripts. One may want to offload the script or job 
to a remote machine which is faster and will continue working even after 
one closes their laptop for the night.

To demonstrate this remote compute capability we start by writing a 
‘CPU heavy’ script where we print the date every hour. After we start 
the script we show it still runs in the background after we logout of 
the remote machine. We also show that we can run the job without ever 
logging into the remote machine.

# Approach
To begin we write a script that will run for an extended period of time. 
Using a combination of commands ‘sleep’ and a loop we run the job for a 
long time. The command ‘sleep’ tells the script to wait for the amount of 
time specified. The value can be in terms of seconds, minutes or hours. 
In our script we tell it to sleep for one hour and loop ten times. Each 
time we loop we output the date to `stdout` using the command ‘date’. This 
looping script simulates a script that is ‘CPU intensive’ where we expect 
the computation to take hours. Using this script we can test remote 
computing capabilities.

Next we monitor the status of our job in real-time. We want to output our 
`stdout` stream to a file instead of the terminal screen. `Nohup` allow us to 
redirect our `stdout` steam to a file which we will call `hw05.out`. We also 
output `stderror` to a file to catch any errors that may occur as our script 
runs. Lastly we need to disconnect our processor of running the script 
from our current shell otherwise when we log out all child processes of 
our shell will also quit. The following command will let us accomplish 
all the above concerns.

``` shell
$ nohup <path/to/script>/hw05.sh > hw05.out 2> hw05.err < /dev/null &
```

`Nohup` allow us run a job that won't be interrupted by hangups. Therefore 
when we disconnect our shell and it sends a HUP signal to all child 
processes our processes will not terminate. To have our `stdout` saved we 
output to a file called `hw05.out`. The second output argument is the 
`stderror` steam which we can also redirect to a file. All other outputs we 
output to `/dev/null` which will ensure our script runs successfully. 
The `&` at the end of the command allows the script to run in the background. 


[Click here for full report.](
http://files.tdevin.com/blog/20150928_trejo_devin_hw05.pdf)