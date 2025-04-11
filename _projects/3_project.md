---
layout: page
title: DPV
description: Diver Propulsion Vehicle
img: assets/img/3_project/1.jpg
importance: 1
category: Fun
related_publications: false
date: 2024-06-12
toc:
  sidebar: left
---

<h3>Introduction</h3>
My Diver propulsion vehicle (DPV) has been a work in progress for sine the fall of 2022. A DPV is a means of aiding transportation under water for divers, they are also offen called underwater scooters. It is a project i have undertaken mostly for the challange of making it, but that i do plan on using it doing fun dives. 

<h3>Design</h3>
I chose to design the DPV around a water jet concept, this was to try and keep the DPV small and compact. The main body is built using an Aluminum pipe with a dimension of 106 mm x 3mm, This pipe is used both as the main body tube and the inlet section of the waterjet drive. The watertight bulkheads on both ends of the main body tube is turned in POM

<h3>Parts</h3>

A small walkthrough of parts from the nose moving backwards. 

<h5>Nose cap</h5>
The nose cap is uaed as a watertight bulkhead in the from of the main body tube. The complete nose cap consists of a turned cap made from black POM. This part has has a few features to enhance its function. On the front it has a bolt flange pattern, this allows the mounting of other parts to the front, that can easily be changed, at the moment it is used for a 3d-printed handel. To seal against the inside of the body tube the nose cap has 2 oring groves for redundancy. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/noseCap1.jpg" title="NoseCap mounted in body tube" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/noseCap2.jpg" title="crosssection of nosecap" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
</div>
<div class="caption">
    Left: Nose cap mounted in body tube. Right: Cross section of nose cap.
</div>

<h5>Motor</h5>
The motor used in the DPV is a [5065 270KV BLDC motor from flipsky](https://flipsky.net/collections/hobby-motors-for-esk8-ebike-efoil/products/electric-skateboard-motor-bldc-5065-270kv-1550w) and the ESC to drive the motor is the [Mini v6 MK5](https://flipsky.net/collections/v6-series/products/mini-v6-mk5-with-power-button) this is a VESC based speed control that allows fine control of the drive parameters. The Motor is mounted on a CNC-milled aluminum bracket. And uses a flexible shaft coupling to connect the the driveshaft of the drive. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/motor1.jpg" title="Motor mounted in the DPV" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/motor2.jpg" title="Motor isolated" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
</div>
<div class="caption">
    Left: Motor mounted in the DPV. Right: Motor isolated.
</div>

<h5>Rear bulkhead</h5>
The rear bulkhead is by far the most complicated part of the DPV. It is made as a turned part from black POM. As the nose cap is has two o-ring groves to seal with the main body tube. other then that it has a M26x1.5 thread to screw in the drive shaft tunnel. It also has several diffrent bolt patterns that are used to mount the inlet section, handle, and the motor mount. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/rearbulkhead1.jpg" title="Isolated rear bulkhead" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/rearBulkhead2.jpg" title="Cross section rearbulk head" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
</div>
<div class="caption">
    Left: Rear bulkhead. Right: Cross section of rear bulkhead.
</div>

<h5>Waterjet Drive</h5>
The waterjet drive is the rotating heart of the DPV. This part sucks water in through the inlet, accelerates it to high speed, and pushes it out of the nozzle. It consists of several parts: the driveshaft, shaft tunnel, impeller, thrust ring, and stator/nozzle.

The shaft is a turned stainless steel shaft. It connects the impeller with the motor. To pass through the rear bulkhead, be watertight, and still allow rotation, it uses the following [mechanical seal](https://www.aliexpress.com/item/1005004226987547.html). The shaft is also supported by three bearings: two ball bearings at each end and a needle roller bearing in the middle at the seal. The impeller is a 76 mm 3D-printed part, printed in a polycarbonate blend for strength. The trust ring is a 3D printed ring used as the tube around the impeller and as a connection between the inlet tube and the nozzle. The nozzle is 3dprinted and also has an internal stator to help make the flow uniform from the nozzle.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/drive1.jpg" title="Drive outside" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/drive2.jpg" title="Nozzle showing stator" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/drive3.jpg" title="Impeller" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
</div>
<div class="caption">
    Left: General overview of rear end Middle: Nozzle showing stator Right: 3-bladed impeller.
</div>

<h5>Handel and controls</h5>
To guide and control the DPV under water there is a single handel, this is only used to sear and control the DPV while a strap connectest to the BCD of the diver that is then towed by the DPV. The handel and contorles consists of 2 CNC milled aluminum parts, a turned POM part and a mountain bike handel bar grip. The two aluminum parts are the main support and then the trigger to operate the DPV. The trigger works by triggering an internally mounted reed switch using magnets mounted to the trigger. This single trigger allows the user to change between safe and drive mode, change speed setting and run the motor. For monitoring the Battery state and speed setting, 2 RGB LEDS are used.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/handel1.jpg" title="trigger" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3_project/handel2.jpg" title="main handel" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
</div>
<div class="caption">
    Left: Trigger Right: Main handel support.
</div>
