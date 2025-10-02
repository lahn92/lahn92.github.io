---
layout: page
title: VOCAB
description: Volatile Organic Compounds Autonomous Boat
img: assets/img/vocab/1.jpg
importance: 1
category: Work
related_publications: false
date: 2025-07-15
toc:
  sidebar: left
images:
  lightbox2: true
---


<h3>Introduction</h3>
This project was developed as part of my work at Aarhus University. It began as a student project, which our department took over after its initial completion. Our work focused on finalizing the project. Some subsystems needed to be built from scratch, while others required fine-tuning. The boat will be used in climate research to measure the diffusion of VOCs from the surface of the ocean to the atmosphere.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/1.jpg" lightbox=true lightbox_group="vocab" title="Boat in water" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The boat doing a field test. 
</div>

<h3>Requirments</h3>
The requirements for the system are listed below. These are the main requirements used to fully develop a product specification. A process was followed in collaboration with the project recipient to ensure all aspects were covered in greatr detail then provided here.

- Max footprint in transport configuration of 1200 X 800 mm to allow transport on standard euro pallet.
- Endurance of 72+ hours deployed. 
- Sattelite communication for remote monitoring.
- Only apporoved materials to avoid VOC contamination. (316L stainless, 5754 aluminum, PMMA, polycarbonate, PTFE, HDPE and PEEK to name a few)

<h3>Work needed</h3>
When the project arrived in our department, the system had already been tested with a fair amount of success. This provided us with a solid starting point. As a result, the scope of our work was relatively limited. The main tasks included:

- Power system: Due to time and budget constrains for the students. A battery system to allow for the 72hr endurance was not fitted.
- Sampling chamber: The student supplied sampling chamber consisted of unglued finger jointed PMMA sheets and as such was not air tight. 
- Legal requirments: Working with the danish maritime autroities to work out the requriments to allow the deployment of the system in a legal way.
- Software refinement: The onboard software still needed some subsystems implemented and others refined. 
- Testing and validation: 


<h3>Power system</h3>
The power system was developed together with the power system for [ARCMETIS](/projects/6_project/). This means that, other than the battery capacity, they are more or less equal. One of the risks was whether we would be able to get a battery that would allow the system to be shipped by air freight, as this would be needed if the system were to be deployed to Greenland. After talking to AirGreenland, we were told that shipping the system with the specified battery system consisting of four 12V 40Ah LiFePO₄ batteries won't be a problem. As such, the selected batteries ended up being [PQ-LFP1240A](https://actec.dk/batterier/genopladelige-batterier/lithium-jern-fosfat-lifepo4-batterier/12v-12-8v-40ah-512wh-lifepo4-paqpower-batteri)

<h5>Power Wiring</h5>
The battery system as mentioned consists of four batteries. In the boat they will be placed two in each hull. In each hull the batteries will be wired in series to get a 24V system. And then the hulls are connected in parrallel, allowing each hull to power the other in case of a failure.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/batteries1.jpg" lightbox=true lightbox_group="vocab" title="batteries" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The batteries wired in series and mounted in the hull. 
</div>

To allow the system to be prepared at shore before deployment with out draining the batteries, each hull also have a battery main disconnect mounted allowing the system to be powered up or down without disassembly.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/batteries2.jpg" lightbox=true lightbox_group="vocab" title="switches" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The battery disconects mounted on the front of each hull. 
</div>


<h3>Sampling Chamber</h3>

The sampling chamber is a clear plastic dome mounted on the front of the boat, its used to enclose a volume of air. In to whice VOCs can difuse from the water surface in the the volume to then be sampled by the systems. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/dome.jpg" lightbox=true lightbox_group="vocab" title="switches" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Picture showing the dome mounted on the boat
</div>

The dome consists of 3 pieces, one top dome with and interface flange mounted, a bottom dome the extends into the water to protected agianst water movement and finally a mounting bracket, that secures the chamber to the boat.
<h5>Domes</h5>
Both the top and bottom dome starts out as a blowen dome. for the top dome a smaller diameter at the top is cut out and a bolt pattern drilled to allow for the mounting of the flange, the flanges job is to give a flat surface for connections to the sampling system. the flange consists of an inner and an outer aluminum piecs that gets bolted througe the dome and sealed with viton o-rings. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/flange.jpg" lightbox=true lightbox_group="robot" title="Link A" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/flange.jpg" lightbox=true lightbox_group="robot" title="Link B" class="img-fluid rounded z-depth-1 custom-img" %}
    </div>
</div>
<div class="caption">
    Left: The mounted flange. Right: Cross section of the flange.
</div>


<h3>Legal requirments</h3>
A problem i encountered during the project is that a remotely operated boat, that is left without direct supervision for extended periodes of time, is in a legal grey zone in denmark. So during the project i was in contact with the danish maritime artorities.
They help us figure out what kind of clasefication the system needed to be operated in a legal manner. The final result for this was that the vessel would be registered as a "non anchored bouy" with mesurements equiment onboard. Meaning it needed to be marked with a yellow blinking light and a yellow X. 
