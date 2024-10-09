---
layout: page
title: Cycloid Clock
description: A customed designed clock based on a cycloidal drive.
img: assets/img/cycloid/thumbnail.png
importance: 2
---
-----
## Motivation
At one point, I remember being shown a picture of a gear themed clock, and being rather annoyed that despite clocks running on gears, and this clock being gear themed, it's "pretty" gears didn't _do_ anything for the mechanism. Ever since, I've had the idea in the back of my head to design a clock where all the functional gears are clearly visible.

It was during my final project for a CAD course that I decided to actually have a go at it, and came up with a design based on [cycloidal drives](https://en.wikipedia.org/wiki/Cycloidal_drive). Specifically, I was inspired by [Levi Janssen's](https://www.youtube.com/watch?v=6xoCeliJ11Q) video showing a design for a single-plane, multistage cycloidal gearbox, and based my design for a clock of this style of gearbox.

## Initial Design
<div class="row mt-3 justify-content-sm-center">
    <div class="col-md-6 mt-md-0">
        {% include figure.liquid path="assets/img/cycloid/solidworks-asm.png" caption= "First revision of the cycloidal clock" title="First version of cycloidal clock" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
I was able to come to a design I was happy with by the project deadline, but the clock was rather large, had power or drive system, and was not particularly manufactuable. However the mechanism itself was functional, and it served the purposes of the class project, which did not require me to actually build my design.
Since that class focused on comparing 2 CAD softwares - CREO Parametric and Solidworks, I modeled my design and produced drawings in both, which are shown below. I find it interesting to compare the differences in visual style between the two softwares - CREO's drawings(left) are much more striking.

<div class="row justify-content-sm-center">
    <div class="col-md-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/cycloid/Creo-Drawing.png" title="Creo Drawing of clock mounting plate" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-md-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/cycloid/Solidworks-Drawing.png" title="Solidworks Drawing of clock mouting plate" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
## Revisiting
More recently, I decided to go back and work to redesign the clock into something both manufactuable  and beautiful. The design I came up with uses stainless steel sheet for the gears, held onto the back plane with magnets and driven by a small stepper motor. I managed to shrink the design somewhat, which was aided by designing the gears to be more parametric, making iteration on gear profiles and sizes much quicker.
This design is meant to be constructed out of steel plate, with the gears held onto the back plane by magnets to make for an extremely minimal design. The cad for this version was done using Onshape, [and is available online](https://cad.onshape.com/documents/6c451e4294f56b11346f6eca/w/8283c5e1aac9d7144dc17c54/e/ba40aee599be0f51e1387e2e?renderMode=0&uiState=658b97496f79aa00b39778c0) I hope to begin prototyping this design shortly.

<!-- <iframe src="https://www.youtube.com/embed/a6Xn4TR0WDk" width="640" height="480"></iframe> -->

<div class="justify-content-sm-center"> 
  <iframe src ="https://www.youtube.com/embed/vTKVgvDKzgA?playlist=vTKVgvDKzgA&loop=1" width="100%" max-width="90vw" height="600px"></iframe>
</div>
