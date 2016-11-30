---
layout: post
title: Broadband-Hamnet Microwave Communication System
subtitle: ENGR 4296 - Senior Design
categories: TempleU
tags: [networking, mesh, routing, programming, software, linux, school, server, bash, python]
bigimg: /img/posts/senior_design/toichat_cover.jpg
---

- [Project Website](
https://sites.google.com/a/temple.edu/broadband-mcomm/)
- [Project Poster](
http://files.tdevin.com/blog/20160416_fdr_review_poster_final.pdf)
- [Project Final Design Review Powerpoint](
http://files.tdevin.com/blog/20160416_fdr_review_pptx_final.pdf)
- [Project Video 1 - Command Line Interface Demonstration](
https://www.youtube.com/watch?v=_-q7M_saQdkA)
- [Project Video 2 - Graphic Interface](
https://www.youtube.com/watch?v=DbUwcBYxRT)


# Abstract
Our Broadband-Hamnet Microwave Communication System (BHMCS) is an inexpensive
alternative to traditional HAM radio equipment that is still reliable to 
use in emergency situations. We will use readily available Linksys WRT54G
routers to setup a long distance communication network that is
self-configuring allowing users to easily find one another. In the process
of creating a self-configuring network we create a new network protocol
termed remote machine discovery protocol (RMDP). At the heart of the
project is a Raspberry Pi 2 processor, which will handle all
half-duplex/full duplex communications. Knowledge of data communication
and transmission, statistical bit error correction, antenna design, and
network programming are required to complete project. We hope our project
will successfully supplement the Amateur Radio community’s radio network
in the Philadelphia Area.


# Executive Summary
Broadband-Hamnet Microwave Communication System aims to provide
long-distance emergency communications using low-power, portable, and
inexpensive equipment. In an environment where cell reception and internet
access becomes unavailable, it is important to maintain a means of
communication to an area outside the area in distress. This project will
also be useful in places where there is a lack of an Internet Service
Provider (ISP). These countries can use this project to communicate
wirelessly within their borders, as well as internationally. This project
aims to be a low-cost, and reliable solution to this issue.

In order for this project to be successful, the hardware needs to be
readily available and inexpensive, and the software must be user-friendly.
In an environment where power may become unavailable, the equipment must
consume a small amount of power, provided from an external battery or
backup generator. The system must also automatically and dynamically
re-configure itself due to the possibility of pre-existing nodes becoming
unavailable in emergency situations and new nodes becoming available. The
communication protocol implemented in the design must also have sequencing,
error detection/correction, and automatic repeat request functionality.

For the reasons described above, the system will consist of a Raspberry Pi
model 2, and a Linksys WRT54G wireless router. The routers will be
programmed, (flashed) with a custom firmware known as Broadband Hamnet. The
Broadband Hamnet firmware takes care of configuring the mesh network, which
includes an optimized link state routing (OLSR) protocol, digi-peating,
and discovering new nodes (new routers that come one the air). The firmware
does not account for devices connected to LAN network of the nodes. Because
of this, communication cannot be made between two users of the network.
Therefore, it is necessary to design an application that automatically
finds the IPv4 addresses of remote machines connected to the mesh network.
The routers run a bare-bones Linux operating system, allowing the use of
existing tools such as the address resolution protocol (`ARP`) and networking
utility `netcat` as the basis for the new remote machine discovery protocol
(RMDP). In order to ensure that there is not a single point-of- failure in
the mesh network, each Raspberry Pi will act as a server and client. It
allows every single machine on the network to know how to contact any
other machine on the network. The machines will communicate using
Transmission Control Protocol/Internet Protocol (TCP/IP) as the underlying
protocol. It is necessary to design an application protocol so that each
machine can process and reply to different types of messages. The different
types of messages include new node discovery, network information requests,
peer-to-peer communication requests and priority messages. The application
protocol will be developed using Google’s protocol buffer (Protobuf)
encoder. To increase maximum distance between nodes, a Yagi antenna will
be connected to the Linksys WRT54G through a coaxial cable. A Yagi antenna
is a unidirectional antenna that redirects most of the signal energy in
one direction. This concept increases transmission distance without any
additional power requirements.

This project is very likely to be completed in its entirety within the
allotted time period. The success of the Broadband Hamnet Microwave
Communication System relies heavily on the community because multiple nodes
are required for a successful mesh network. If successful, this project
could supplement emergency communications in the Philadelphia area.
Because the project is open source, only the initial investment of under
$100 is required to set up a node in the mesh. In order for the mesh to be
effective, the network needs to span a large area. Covering a large
geographical area is possible, especially because a Raspberry Pi 2 is not
needed at every mesh node. The Linksys WRT54G flashed with the Broadband
Hamnet firmware can act as a repeater station, which simply forwards
messages for other nodes. Because the Linksys WRT54G is only around $40,
nodes can be installed to cover a large geographical area, without the
help of large power amplifiers and antennas. The Broadband Hamnet 
Microwave Communication System also has the ability to provide
underprivileged areas with an inexpensive way to communicate with family
and friends because the equipment is so inexpensive and accessible.

[Click here for full design document.](
http://files.tdevin.com/blog/20160416_sd27_broadband_hamnet_microwave_communication_system_final.pdf
