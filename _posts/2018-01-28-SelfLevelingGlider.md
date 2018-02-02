---
layout: post
title: "Self-Leveling Glider - Controls Project"
date: 2018-01-28
comments: true
---

<!-- Glider image will go here -->

The motivation for this project was to design a control system for a glider that would allow it to correct it's orientation and fly straight and level given any starting angle and any external disturbances.

The system consists of a lipo battery, an inertial measuring unit (IMU), a PID controller, and three servo motors to actuate the control flaps.

This project presented both software and electrical design decisions. In order to power all three servos and the micro-controller, a 12V 1.5A lipo battery was chosen. Each servo is rated at 5V; therefore, a voltage regulator was used to step down the voltage to a constant 5V across each servo. In addition, a raspberry Pi was connected to the circuit in order to feed data from the controller and store it to be able to theoretically assign gain values to our controller in Matlab. The full circuit is shown in Fig. 1.

<!-- Circuit image will go here -->
![Circuit](/images/Glidercircuit.png){:class="img-responsive"}

