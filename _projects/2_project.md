---
layout: page
title: Ball balancing robot
description: 
img: assets/img/2_project/1.jpg
importance: 1
category: Fun
related_publications: false
date: 2024-06-16
toc:
  sidebar: left

---

<h3>Introduction</h3>
This robot is a 3RPS parallel manipulator platform. The platform has 3 degrees of freedom with a spherical joint, allowing the platform to be angled in any direction. The project takes heavy inspiration from the ball balancer project by [Aaed Musa](https://www.aaedmusa.com/projects/project-three-sng7y-gaslp). The project was started in late summer of 2023, with the intention of bringing it to the Aarhus Maker Faire as an exhibition for the Open Space Aarhus stand.
<h3>Mechanics</h3>
The mechanical linkage of each of the three arms consists of two different links: Link A, which connects to the shaft of the stepper motor and has a pin joint connection with Link B, which further connects to the platform with a ball joint. The original intention was that both joints would be CNC-machined out of aluminum, with the CNC-machining done on a Pocket NC 5-axis mill. However, Link B was too long for the travel of this machine, and as such, the design of Link B was changed to consist of a piece of carbon fiber pipe, with machined endcaps for the two joints. Other parts, such as the platform, main body, and casing, were 3D-printed.
<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2_project/2.jpg" title="Link A" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2_project/3.jpg" title="Link B" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Link A. Right: Link B.
</div>

<h3>Electronics</h3>
The electronics consist of three 1.8-degree stepper motors, driven by a BigTreeTech TMC2209 stepper driver and a Teensy 4 microcontroller controlling it all. To provide the controller with feedback on the ball’s location, a glass 4-wire resistive touch interface is used. Two step-down converters are employed to reduce the 12V DC input to 5V and 3.3V for use by the different components.
<h4>PCB</h4>
To connect all the electronics together, a custom PCB was designed. The PCB has 4 layers in a signal-ground-power-signal stackup. In addition to accommodating the various components, the PCB features connectors for the stepper motors, the touch interface, and a few potential buttons. Screw terminals are also provided for power input. This design allows the electronics to maintain a clean appearance while remaining easily disassembled.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2_project/4.jpg" title="PCB" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The finished PCB.
</div>

<h3>Software</h3>
The software uses the excellent library by Aaed Musa for the inverse kinematics. To actually regulate the ball's position, the robot uses a PID algorithm. This algorithm consists of:

* Error - The distance the ball is from the setpoint of the PID algorithm.
* Proportional Term (P) = kp * Error - An output that is proportional to the error.
* Integral Term (I) = ki * ∫error - An output that accumulates the error over time.
* Derivative Term (D) = kd * (d/dt) * error - An output that is essentially the speed at which the position of the ball changes.
* Output = P + I + D - The output is essentially the most effective way to get the ball back to the center.

Using the PID algorithm, the robot is constantly trying to move the ball back to the setpoint for where the ball should be. The PID algorithm is tuned by adjusting the constants kp, ki, and kd, thus changing the magnitude of each output of the PID algorithm. In total, the controller is running 2 PID algorithms, one for the X and one for the Y direction.

<h3>To be done</h3>
A small list of things still to be done:

<h4>New touch interface</h4>
Sadly, the touch interface broke a few days before the Aarhus Maker Faire, so the robot only got to play as an advertising stand with an Open Space Aarhus logo on top. The current plan is to purchase an interface, preferably bigger, to allow more area of movement for the ball.

<h4>Rewrite software</h4>
During the integration hell part of the project, I had to make significant changes to the code to get it to work, resulting in a messy code base. I would like to get this rewritten and cleaned up.