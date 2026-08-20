---
layout: post
title: Robomaster Sentry Turret
date: 2025-06-24 00:00:00 -0700
description: I designed and manufactured the turret of the Sentry Robot for the 2025 Robomaster North America Robotics Competition. # Add post description (optional)
img: Sentry2025.jpeg # Add image post (optional)
tags: [Solidworks, 3DPrinting, Waterjet, DFM] # add tag
---

Designed and manufactured the turret of our University team's Sentry Robot for the 2025 Robomaster North America (RMNA) Robotics Competition.

**Results:**
- Capable of indexing and firing at 1500 rounds per minute at 84% accuracy
- Achieve Pitch and Yaw control with 2 BLDC motors
- Fibreglass composite construction made from waterjet plates

![Turret Cross Section]({{site.baseurl}}/assets/img/Turret_Cross_Section2.png)
Cross Section of the ball path from the indexers through the hollow pitch motor and into the flywheels

Firing test for a 3D printed prototype of the Sentry
(todo: video of assessment)

**Challenges:**
- Many, many indexer iterations were tested and scraped due to projectiles jamming at high indexing speeds. Ultimately, an indexer with a spiral path was chosen to allow the indexing motor to reverse direction to clear jams
- High MOI made tuning the yaw rotation difficult
![Spiral Indexer]({{site.baseurl}}/assets/img/Spiral_IndexerV2.png)

**Background:**
[RoboMaster](https://www.robomaster.com/zh-CN) is an international robotics competition organized by the drone company DJI in which University teams design, build, and compete with ranged combat robots in an Esports style competition. Each robot must be built from the ground up integrating custom mechanical components, electronics, embedded controls, and high-level software such as computer vision.

One of the Robot types in RoboMaster is the Sentry, which must autonomously detect, engage, and fire upon the "armour plate" sensors on other robots. It features two 17mm barrels mounted on a turret which must be able to pitch, yaw, and direct plastic pellets towards targets.