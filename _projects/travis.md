---
layout: page
title: Balance Bot
description: A custom-designed balancing robot using teensy and C++
img: assets/img/travis/travis-open(thumb).jpg
importance: 1
---
-----
<div class="row justify-content-sm-center">
    <div class="col-md-4 align-self-center">
        {% include figure.liquid path="assets/img/travis/travis-closed.jpg" title="Balancing robot, Travis" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-md-4 align-self-center">
        {% include figure.liquid path="assets/img/travis/travis-open.jpg" title="Balancing robot, Travis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
My senior year of high school, I requested an independant study in robotics, with my primary project being the design of a 2 wheeled balancing robot. I designed this robot(eventually dubbed Travis) from scratch, with the goal being to have it balance itself on two wheels and be controlled over bluetooth from my phone. This project ended up taking the entire year, and while it was balancing by the end of the year, it required constant attention and trimming to keep it in one place. After graduating, I've continued to iterate on the design, attempting to make it balance more robustly.

I designed the chassis and electronics myself, using Autodesk Fusion 360 for the mechanical parts, and a tool called [DIY-LC](https://bancika.github.io/diy-layout-creator/) to plan the electronics. In hindsight, there are much better ways to have planned the electronics, but this got the job done at the time and allowed me to plan how I would lay things out on the perf-board. The main controller is a teensy LC microcontroller, which I programmed using the Arduino framework, and paired with a bluetooth chip, an accelerometer/gyroscope, and a motor driver. The bot could sense it's pitch angle using the accelerometer and wheel rotation from the encodors on the drive motors, and from this information a balancing controller could keep it upright.
<div class="row justify-content-sm-center">
    <div class="col-md-5 align-self-center">
        {% include figure.liquid path="assets/img/travis/BalBotTeensy.png" title="the electronics diagram for Travis" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-md-5 align-self-center">
        {% include figure.liquid path="assets/img/travis/cad.png" title="CAD design of 3D printed shell" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The robot code is written in C++, using the Arduino libraries for the teensy, and uses a PID controller to balance the robot based on the bluetooth input and sensor readings. 
Travis can connect to any bluetooth device, and initially was programmed to interface with a customizable bluetooth control app I discovered. 
I was learning C++ as I wrote the code for this project, and while I learned a lot through this process, it did mean I ended up rewriting large chunks of the code many times over. The current code for the bot is on github, linked in the tile below.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-sm-center">
    {% include repository/repo.liquid repository="nWestie/BalanceBot" %}
</div>
<div class="row justify-content-sm-center">
    <div class="col-md-8 align-self-center">
        {% include figure.liquid path="assets/img/travis/phone.png" title="Phone Controller" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
More recently, I wrote a custom python interface for windows, which makes it easier to update and tune the PID constants on the fly, as well as logging data from the robot for later analysis. 
The app is written in python using [Kivy](https://kivy.org) for the UI, and connects over bluetooth serial to the robot, much like the phone controller. 
Having logs of all the accelerometer and encoder data from the bot makes it easier to tune it's performance, measure change over time, and see exactly what the bot was measuring at times when it behaved undesirably. This python project hosted on github in the project below.
<div class="repositories d-flex flex-md-row justify-content-sm-center">
    {% include repository/repo.liquid repository="nWestie/BalBotClient" %}
</div>
<div class="row justify-content-sm-center">
    <div class="col-md-8 align-self-center">
        {% include figure.liquid path="assets/img/travis/desktop.png" title="Completed 3D construction model of the set" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
Currently, my goal is to use this new interface to refine the movement of Travis, hopefully using the encoders to allow it to hold position without drifting, make turns, and limit its acceleration to prevent itself from falling over. I have begun re-writing the PID controller and other parts of the bot-side code to make this happen, but it is still a work in progress.