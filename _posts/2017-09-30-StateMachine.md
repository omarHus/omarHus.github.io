---
layout: post
title: "Ignition State Machine - Uottawa Rocketry"
author: "Omar Husain"
date: 2017-09-30
comments: true
cover-photo: "/assets/images/rocket.jpg"
photo: "/assets/images/rocket.jpg"
photo-alt: "/assets/images/rocket.jpg"
---

For two semesters I joined the uOttawa Rocketry team and I was able to participate in various aspects of the rocket's design. Our goal was to build a hybrid rocket (liquid oxidizer, solid fuel) that would achieve a target apogee of 10,000ft, as part of the Intercollegiate Rocket Engineering Competition.

I designed and wrote the software for the ignition system of the rocket. The system consisted of an igniter relay, control valve, microcontroller and wireless communication via a Xbee. To control the system from a safe distance I designed a state machine which used serial input to engage specific commands in the ignition sequence. The different states of the system are shown in the table below. 

<br>
<center></center>

|---|---|---|
|State| |Number| |Action|
|:---:| |---| |:---:|
|`STOP`| |1| |Close the valve, turn the igniter relay off.|
|`IGNITE`| |2| |Turn the igniter relay on, starting the igniter.|
|`OPEN`| |3| |Keep the igniter relay on, open the valve, keep it open for 10 seconds|
|`CLOSE`| |4| |Close the valve|
|`WAIT`| |5| |Do nothing|
|`PING`| |6| |Send ``"I AM ALIVE!"`` to the base station over the radio|


<br>

The state machine ensures that an acceptable sequence of actions occurs no matter what command is given to the controller. These relationships are typically represented in a state transition map.

<!-- Insert picture of state map -->

The tricky part for this program was to ensure that the system could be turned off at any moment. For a non-wireless system, this is a simple task. There exists a function, called the intercept function, which when called stops all other functions and runs parallel to the current program.  An intercept function could not be called in this case, because the pins on the controller that are used to communicate this call were already being used by the Xbee to wirelessly transmit our serial commands. Therefore, making use of the state machine, the solution was to poll the serial input frequently, so that if a 'STOP' command occured, the system would act immediately.



