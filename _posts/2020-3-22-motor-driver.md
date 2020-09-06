---
layout: post
title: "Arduino Motor Driver Circuit"
date: 2020-3-22
category:
  - Project
image: assets/img/blog/circuit_photo.jpg
full-image: assets/img/blog/circuit_photo_full.jpg
author: Lorenzo
tags: walker-v1
---

Progress update for today: I’ve got the basic motor driver circuit figured out. For the preliminary design and prototype, this is the only system of electronics I need. For now, I’m using an Arduino Uno (just an easy platform to program and send PWM signals), although that may change. Here’s the circuit diagram I’m using:

![Circuit diagram](/assets/img/blog/motor_driver_circuit.png)

I’m not using a professional diagramming software yet, so excuse the poor image quality. The Arduino can output PWM signals on the digital pins with a (~) next to them (labeled PWM in the diagram). I’ve used two MOSFETs (both 200N3LL) that act as switches, allowing the motors to be powered through an external source. Right now, that’s a 5 V regulated source I have, but that stands to change as the device is converted into a portable form.

The 1 kOhm resistors at the gate of the MOSFETs are there to ensure the MOSFETs act as switches. The sources are connected to the common ground, and the drains are connected to each motor, which has a diode for protection. This allows easy PWM control using an Arduino and external power supply.

Now that the circuit is proven, the next step is to assemble the thing. I’ll start with a preliminary Solidworks file and begin building from there. This should allow static and dynamic software testing once construction is complete.
