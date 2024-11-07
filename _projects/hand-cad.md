---
layout: page
title: CAD - Hand
description: A human-like 3D printable hand actuated by strings.
img: assets/img/handcad/asm-white.png
importance: 4
---
-----
<div class="row justify-content-sm-center">
    <div class="col-md-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/handcad/drawing.png" title="detail drawing of the thumb joint" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
The introductory engineering CAD course at Grove City taught PTC Creo Parametric, and as a final project, 
we were asked to work with a group to design and manufacture a small-scale, 3D-printable device of our choosing. 
Our group choose to make a roughly human-scale bio-mimetic hand, actuated by strings and elastic bands. Each group member designed a number of components, and I was responsible for the intermediate finger joint, angled version for the thumb, and creating the assembly of all components.
<div class="row justify-content-sm-center">
    <div class="col-md-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/handcad/asm-white.png" title="assembled hand" class="img-fluid rounded z-depth-1" rough_scale="50vw"%}
        {% include figure.liquid path="assets/img/handcad/thumb-white.png" title="bent thumb joint" class="img-fluid rounded z-depth-1" rough_scale="50vw" %}
    </div>
    <div class="col-md-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/handcad/2joints-white.png" title="2 finger joints" class="img-fluid rounded z-depth-1" rough_scale="50vw"%}
        {% include figure.liquid path="assets/img/handcad/index-white.png" title="intermediate finger joint" class="img-fluid rounded z-depth-1" rough_scale="50vw" %}
    </div>
</div>

The bent thumb joint was especially challenging, as the features needed to be placed at odd angles, and I wanted to design it to be parametric enough to change the thumb-angle without completely redesigning the piece. The design of these joints was quite iterative, and we used our CAD assembly of the hand to inform the design of each component, deciding how far each finger joint should be able to rotate based on how close to the palm they would get when assembled and curled.


I also was responsible for assembling the components of our prototype, which was fully 3D printed except for commonly available cotton cord and elastic band. The design worked nearly as intended when we printed our first prototype - shown below - although because of the somewhat generous tolerances we used when designing, the fingers opened a bit further then expected. To opperate the device, strings run through the loops on the palm-side of the hand to be pulled by an actuator in the wrist, and elastic returns the fingers to an open position. 

<div class="row justify-content-sm-center">
    <div class="col-sm-7 align-self-center">
        {% include figure.liquid path="assets/img/handcad/parts.jpg" title="3D printed components" class="img-fluid rounded z-depth-1" %}
        {% include figure.liquid path="assets/img/handcad/finished-hand.jpg" title="assembled hand" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

