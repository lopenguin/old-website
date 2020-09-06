---
layout: post
title: "Walker in Motion!"
date: 2020-3-27
category:
  - Project
image: assets/img/blog/walker_mk1.jpg
full-image: assets/img/blog/walker_mk1_full.jpg
author: Lorenzo
tags: walker-v1
---

It moves! After many design changes and a few days worth of testing, the prototype is able to move on its “life support” cables! Here’s a quick summary of design changes, as well as the rationale behind them:

![original design](/assets/img/blog/walker_design_full.jpg)

* Addition of a third leg behind for stabilization. When I turned on the motor using the initial circuit, the robot fell backwards immediately. It had nothing to keep it from falling backward when the legs tried to move it forward. With this observation, the bipedal robot became tripedal; I added a third leg that drags behind the bot and stabilizes it when the legs try to push it forwards.

Besides its essential role in stabilizing the vehicle, the third leg provides an opportunity: directional control. With movement on the legs precarious as-is, it may be difficult to turn using only leg motion. The next prototype will be able to rotate its third leg, which acts as a rudder to control the motion of the robot.

* Incorporation of h-bridge chip to enable backwards motion. Using the L293D, an h-bridge motor driver, six Arduino pins can control the speed and direction of the two attached motors. Here’s the circuit diagram, created with a little help from [Adafruit](https://learn.adafruit.com/adafruit-arduino-lesson-15-dc-motor-reversing/lm293d):

![new circuit](/assets/img/blog/walker_circuit_v2.png)

It’s pretty messy looking but not too complicated. A simple digital signal to the in pins controls the direction of current flow through the motor, and a PWM signal to the EN pins controls the speed. I’ve decided to stick with a 5 V power supply because the motors I’m using are not that powerful, and 5 V is actually recommended for them.

The next step with this project is to develop a fully independent model. I’m probably gonna work with the current prototype to mount the Arduino and power supply on the walker. For now, I’ll keep everything in a breadboard until the circuit is finalized, and I won’t draw up another Solidworks design until all the prototyping is done.
