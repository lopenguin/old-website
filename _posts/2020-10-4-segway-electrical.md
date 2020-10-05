---
layout: post
title: "Segway Electrical Design"
date: 2020-10-4
category:
  - Project
image: assets/img/blog/segway_pcb.jpg
full-image: assets/img/blog/segway_pcb_full.jpg
author: Lorenzo
tags: segway
---

I'm building a segway! Sorry last blog post--the walker v2 will have to wait. I was inspired a few days ago to make a segway. It's a controls problem: stabilize an inherently unstable system. There are a lot of tutorials out there on making a "self-stabilizing robot," very similar to this segway robot, but I'm going to do this without using them for guidance and compare my code with theirs at the end. Hopefully this will be something cool and an interesting learning process.

So, as you can tell from the cover image, I have completed the electrical work. I soldered the circuitry onto a perfboard because I wanted it to be small and because the motors need high currents that do not mix well with a breadboard. As with the autocar, I am not going to put the circuit here. The motor control circuit is the same one I've been using (see the walker project), and sensors are just connected via I2C. But, I will show a photo of the current iteration of the design:

![My setup](/assets/img/blog/segway_design_v0.jpg)

More information on how this is organized to come!
