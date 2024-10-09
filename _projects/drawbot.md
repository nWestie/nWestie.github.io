---
layout: page
title: NXT Drawbot
description: A custom pen plotter built with LEGO Mindstorms NXT.
img: /assets/img/drawbot/Dino.jpg
importance: 7
---
<div class="justify-content-sm-center"> 
    <iframe src ="https://www.youtube.com/embed/orBfnTQuWAs" width="100%" max-width="90vw" height="450px"></iframe>
</div>
<br/>

## Overview
This project was the result of suddenly having large amounts of free time as the world initially shut down for COVID in 2020. Some people baked bread, I decided to build a robot. The NXT platform was what I had available at the time, and I built a cartesian gantry capible with a mount for a whiteboard pen.

The heart of the project was the code - I used [NXC](https://bricxcc.sourceforge.net/nbc/), a C based language and compiler built for the NXT, and wrote custom software to read G-code from a file and control the motion of the plotter. I used Fusion 360 to generate G-code, and it handles nearly all of the commands commonly used by 3D printers.


## PC Driver Program
In addition to the robot, I built a command line program to control the robot remotely, connection over USB or bluetooth to stream G-Code files to the robot. This sped up testing by removing the step of uploading G-code to the robot, and allowed for larger g-code files to be used. I also wrote the driver program in C++, and made use of the [NXT++](https://github.com/corywalker/nxt-plus-plus) library to handle all communications with the NXT.

-----
The code for the project is on Github:
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-sm-center">
    {% include repository/repo.liquid repository="nWestie/nxt-drawbot" %}
</div>
<br/>
And some additional example drawings are below:
<br/>


## Trombone Drawing
<div class="justify-content-sm-center"> 
    <iframe src ="https://www.youtube.com/embed/h-ReSmWMP4c" width="100%" max-width="90vw" height="450px"></iframe>
</div>
<br/>

## House Drawing
<div class="justify-content-sm-center"> 
    <iframe src ="https://www.youtube.com/embed/Kh3upxtFZQ4" width="100%" max-width="90vw" height="450px"></iframe>
</div>