---
layout: post
title: "Simulation of Flow Over NACA 0015 Airfoil"
date: 2019-04-27
comments: true
youtubeId: 
cover-photo: "/assets/images/naca_airfoil.png"
photo: "/assets/images/naca_airfoil.png"
photo-alt: "/assets/images/naca_airfoil.png"
---

<!-- image will go here -->
<!-- <center><img src="/assets/images/3Dgearbox.jpg" alt="Portrait" style="width:30%"><img src="/assets/images/worm_gear.png" alt="Portrait" style="width:30%"></center> -->

For my computational Fluid Dynamics class the final project was to solve a set of partial differential equations (equations that depend and change with respect to several variables) for some physical problem using a computer model. I chose to model the flow over a symmetric airfoil (airplane wing) at supersonic speeds (i.e. at speeds many times over the speed of sound.)

<!-- image of NACA 0015 Airfoil goes here-->
<center>
<div class="4u 12u$(mobile)">
    <div class="item">
        <img class="image fit" src="{{ '/assets/images/naca_airfoil.png' | relative_url }}" alt="" />
            <header>
            <h3>NACA 0015 Airfoil Shape</h3>
            </header>
    </div>
</div>
</center>

In the future, as airplane technology continues to be developped, these types of speeds will be possible and so it is important to model this flow. The model is based on the Compressible Euler Equations, which are balance laws based on mass, momentum, and energy conservation for inviscid (no viscosity) flow.

<!-- image of Compr. Euler Equations -->
<center>
<div class="4u 12u$(mobile)">
    <div class="item">
        <img src="{{ '/assets/images/zeroAlpha.png' | relative_url }}" alt="" width="100%" />
            <header>
            <h3>Flow Characteristics at Angle of Attack of 0 deg</h3>
            </header>
    </div>
</div>
</center>

To create the computational mdoel, the shape of the airfoil has to be determined and the space around it has to be divided up into little cells. In each of these little cells, the physics of the flow will be solved. The computer model is told to run for a given amount of time and computes the physics of the flow at a discrete number of time steps. This allows us to show an animation of how the flow develops in time.

<!-- Animation Goes Here -->

The lift produced by an airfoil is based on the pressure difference from the top surface and the bottom surface. If the airfoil is tilted upwards, the pressure on the bottom surface is greater than the pressure on the top surface and the airfoil produces lift.

<!-- image of 10deg Airfoil here -->
<center>
<div class="4u 12u$(mobile)">
    <div class="item">
        <img class="image fit" src="{{ '/assets/images/10pressure.png' | relative_url }}" alt="" />
            <header>
            <h3>Airfoil at an Angle of Attack of 10 degrees</h3>
            </header>
    </div>
</div>
</center>
<!-- <center><img src="/assets/images/10pressure.png" alt="Portrait" class="image fit"></center> -->

In this image, the white part in the middle is the airfoil and the colour map gives an indication of the pressure field of the flow around the airfoil. 