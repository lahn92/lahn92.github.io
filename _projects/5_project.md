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


<h3>Introduktion</h3>
This project was developed as part of my work at Aarhus University. It began as a student project, which our department took over after its initial completion. Our work focused on finalizing the project. Some subsystems needed to be built from scratch, while others required fine-tuning. The boat will be used in climate research to measure the diffusion of VOCs from the surface of the ocean to the atmosphere.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/1.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
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
The battery system as mentioned consists of four batteries. In the boat they will be place two in each hull. In each hull the batteries will be wires in series to get a 24V system. And then the hulls are connected in parrallel. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/batteries1.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The batteries wired in series and mounted in the hull. 
</div>

To allow the system to be prepared at shore before deployment with out draining the batteries, each hull also have a battery main disconnect mounted allowing the system to be powered up or down without disassembly.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vocab/batteries2.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The battery disconects mounted on the front of each hull. 
</div>











<h3>The plan</h3>
My general plan was to upgrade to a backlit screen and add USB-C charging and a battery to the console. Due to the condition of the console, I also decided to change the shell of the GameBoy. I opted for parts from [funnyplaying](https://funnyplaying.com/) as it was possible to get a shell and laminated IPS screen that didn’t require modifying the shell for the screen to fit.

My full list of components:
- [Screen](https://funnyplaying.com/products/3-0-inch-ips-agb-laminated-kit)
- [Shell](https://funnyplaying.com/products/3-0-inch-ips-agb-laminated-kit)
- [USB-C / battery mod](https://funnyplaying.com/products/gba-li-ion-rechargeable-battery-typec-module)
- [button](https://funnyplaying.com/products/agb-custom-buttons)
- [Silicone pads](https://funnyplaying.com/products/replacement-silicone-pads-for-gameboy-advance)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Gameboy/Parts.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The full parts kit.
</div>

<h3>The work</h3>
Due to the selected parts, the amount of work to put the modded GameBoy together was minimal. It only took a short Friday afternoon after work. The most complicated part was the soldering needed for the new display overlay controls, which consisted of three wires that allowed the overlay to be controlled with the GBA buttons instead of the touch sensor built into the screen.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Gameboy/soldering1.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The wires soldered to the new display PCB.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Gameboy/soldering2.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The wires soldered to the GBA PCB.
</div>

After that, it was mostly a matter of putting the parts in the right spots and screwing everything together.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Gameboy/Internals.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The assembled internals 
</div>

<h3>The results<\h3>

Once the back shell was screwed down, I was left with a fully modded GameBoy Advance.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Gameboy/new.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The finished product show the pokemon sapphire start screen.  
</div>

And it glows!

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Gameboy/GID.jpg" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The finished product show the pokemon sapphire start screen.  
</div>

