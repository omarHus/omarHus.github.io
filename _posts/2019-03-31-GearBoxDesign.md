---
layout: post
title: "Gear Box - Mechanical Design"
date: 2019-03-31
comments: true
youtubeId: 
cover-photo: "/assets/images/3Dgearbox.jpg"
---

<!-- image will go here -->
<div class="row">
    <div class="4u 12u$(mobile)">
        <div class="item">
            <img class ="image fit" src="{{ '/assets/images/worm_gear.png' | relative_url }}" alt="" />
                <header>
                <h3>Gear Box CAD Model</h3>
                </header>
        </div>
    </div>
    <div class="4u 12u$(mobile)">
        <div class="item">
            <img class="image fit" src="{{ 'assets/images/3Dgearbox.jpg' | relative_url }}" alt="3d Gearbox" />
            <header>
                <h3>3D Print of the Gearbox</h3>
            </header>
        </div>
    </div>
</div>


<!-- <center><img src="/assets/images/3Dgearbox.jpg" alt="Portrait" style="width:30%"><img src="/assets/images/worm_gear.png" alt="Portrait" style="width:30%"></center> -->

This gearbox design was a group project with Dave Clarke and Humam Shwaikh at the University of Ottawa. Dave Clarke created the beautiful computer aided design (CAD) model above.

The task for this project was to design a speed reducer/gearbox given certain operational requirements. A gearbox is a means of transmitting the rotational power of a motor from one location to another with possibly varying speeds and torques.

The focus was on making a simple, cheap, and compact gearbox. A full analysis of the stresses on the gears, bearings and shafts was conducted, in order to design a gear box that met the given criteria.

The following table shows the criteria given for this particular gear box.

| Design Constraint | Input Power (HP)| Input Velocity (rpm)| Output Velocity (rpm)|
|-------|--------|---------|---------|
| Vertical to horizontal | 5 | 750 | 80 |

This corresponds to a speed reduction of 9.375. This is a relatively high reduction, so to achieve it in one step a worm gear was used with a triple thread and a wheel with 29 teeth. This corresponds to a speed reduction of 9.67, which is very close to our design requirement. A worm gear also transmits the rotation from a vertical to horizontal shaft, which meets our design constraint.

<!-- image will go here -->
<center><img src="/assets/images/worm_gear_transparent.png" alt="Portrait" style="width:40%"></center>
<center><h3>Gearbox Final Design</h3></center>

My principal task was to analyse the shafts in this gear box. The worm gear generates axial, transverse and radial forces on the shafts. The shafts can be modeled as simply supported beams with a center load. This means that a large bending moment is generated within the shaft at the center and has the following profile.

<!-- image will go here -->
<center><img src="/assets/images/bmd.png" alt="Portrait" style="width:40%"></center>
<center><h3><b>Shear and Bending Moment Diagrams of Shaft</b></h3></center>

The length of the shaft is set by the gear analysis and the bearing analysis. The shaft length is minimized in order to maintain a compact volume and to reduce the bending moments in the shaft. The design parameter of the shaft is therefore the diameter.

Since a gear box is subject to repeated cycles, the main mode of failure to be expected is fatigue. The modified Goodman criterion is used to determine the shaft diameter that will prevent fatigue failure. This criterion considers the mean and alternating principal stresses induced in the shaft and the material properties of the material selected in order to determine the diameter of the shaft at key locations.

<!-- image will go here -->
<center><img src="/assets/images/goodman.png" alt="Portrait" style="width:40%"></center>
<center><h3>Modified Goodman Criterion</h3></center>

The main requirement is that the tortional deflection or angle of twist of the shaft not exceed 0.08 &deg;/ft. By increasing the diameter of the shaft the moment of inertia is increased, which increases the resistance to twisting induced by the tortional loads on the shaft. Basically, having a chubbier shaft prevents the shaft from twisting too much and ultimately failing.