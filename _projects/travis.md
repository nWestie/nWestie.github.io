---
layout: page
title: Balance Bot
description: Custom balancing robot using teensy and C++
img: assets/img/travis/travis-closed.jpg
importance: 1
---
<div class="row justify-content-sm-center">
    <div class="col-md-4 align-self-center">
        {% include figure.html path="assets/img/travis/travis-closed.jpg" title="Balancing robot, Travis" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-md-4 align-self-center">
        {% include figure.html path="assets/img/travis/travis-open.jpg" title="Balancing robot, Travis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
As an independent study my senior year of high school, I decided to create a 2 wheeled balancing robot. This robot, eventually dubbed Travis, was designed from scratch, with the goal of being able to balance itself vertically, and be controlled over bluetooth from my phone. This project ended up taking the entire year, and while it was balancing by the end of the year, it required constant attention and trimming to keep it in one place. After graduating, I've continued to iterate on the design, attempting to make it balance more robustly.

I designed the chassis and electronics myself, using Autodesk Fusion 360 for the mechanical parts, and a tool called [DIYlc](https://bancika.github.io/diy-layout-creator/) to plan the electronics. In hindsight, there are much better ways to have planned the electronics, but this got the job done. The main computer is a teensy LC, programmed using the Arduino framework, and this communicates with a bluetooth chip, an accelerometer/gyroscope, the motor driver, and the motor encoders.
<div class="row justify-content-sm-center">
    <div class="col-md-5 align-self-center">
        {% include figure.html path="assets/img/travis/BalBotTeensy.png" title="electronics diagram for Travis" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-md-5 align-self-center">
        {% include figure.html path="assets/img/travis/cad.png" title="CAD design of 3D printed shell" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The robot code is written in C++, using the Arduino libraries for the teensy, and uses a PID controller to balance the robot based on the bluetooth input and gyroscope readings. Travis can connect to any bluetooth device, and initially was programmed to interface with a customizable bluetooth control app I discovered.
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-sm-center">
    {% include repository/repo.html repository="nWestie/BalanceBot" %}
</div>
<div class="row justify-content-sm-center">
    <div class="col-md-8 align-self-center">
        {% include figure.html path="assets/img/travis/phone.png" title="Phone Controller" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
More recently, I wrote a custom python interface for windows, which makes it easier to update and tune the PID constants on the fly, as well as logging data from the robot for later analysis. The app is written in python using [Kivy](kivy.org) for the UI, and connects over bluetooth serial to the robot, much like the phone controller.
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-sm-center">
    {% include repository/repo.html repository="nWestie/BalBotClient" %}
</div>
<div class="row justify-content-sm-center">
    <div class="col-md-8 align-self-center">
        {% include figure.html path="assets/img/travis/desktop.png" title="Completed 3D construction model of the set" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
Currently, my goal is to use this new interface to refine the movement of Travis, hopefully using the encoders to allow it to hold position without drifting, make turns, and decelerate itself before it is at risk of falling over.