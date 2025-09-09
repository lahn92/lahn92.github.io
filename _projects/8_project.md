---
layout: page
title: Tool2DXF
description: From photo to DXF — digitize your tools in seconds. 
img: assets/img/tool2dxf/1.jpg
importance: 1
category: Fun
related_publications: false
date: 2025-09-09
toc:
  sidebar: left
images:
  lightbox2: true
---

<h3>Introduction</h3>
My [Tool2DXF](https://github.com/lahn92/ToolToDXF) software takes a simple photo of a tool placed on a sheet of paper and automatically extracts its outline as a scaled DXF file ready for CAD or CNC use. The process begins by detecting the rectangular paper sheet in the image and using its known dimensions to calibrate scale. The photo is then perspective-corrected so the paper appears flat and true to size. After calibration, the software isolates the tool from the background, finds its contour, and allows interactive refinement through a built-in editor where you can adjust or redraw parts of the outline if needed. Once the outline is finalized, the contour is converted into real-world millimeter coordinates, offset if desired, and saved as a closed polyline inside a DXF file. Along the way, debug images of each step are saved, making it easy to verify the detection process. This workflow ensures accurate, scaled outlines from just a single photo, making it ideal for digitizing tools or parts for design and manufacturing.
if you find this interresting check it out at the following link: https://github.com/lahn92/ToolToDXF



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tool2dxf/animation.webp" lightbox=true lightbox_group="wind" title="side view" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Animation showing the steps of Tool2DXF
</div>
