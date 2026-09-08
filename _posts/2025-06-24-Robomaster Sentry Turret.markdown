---
layout: post
title: Robomaster Sentry Turret
date: 2025-06-24 00:00:00 -0700
description: I designed and manufactured the turret of the Sentry Robot for the 2025 Robomaster North America Robotics Competition. # Add post description (optional)
img: Sentry2025.jpeg # Add image post (optional)
tags: [Solidworks, 3DPrinting, Waterjet, DFM] # add tag
---
**Designed and manufactured the turret of our University team's Sentry Robot for the 2025 Robomaster North America (RMNA) Robotics Competition.**
 
**Results:**
- Capable of indexing and firing at 1500 rounds per minute at targets
- Achieves Pitch and Yaw aim control with 2 BLDC motors
- Final construction made from waterjet-cut fibreglass composite plates and 3D printed PPA-CF
- Electrically connects to the chassis through a pogo pin PCB

Firing test for a 3D printed prototype of the Sentry
![3D_Printed_Prototype_Test_Gif]({{site.baseurl}}/assets/img/Sentry_Assesment_2025_gif.gif)

**Challenges:**
- Many, many indexer iterations were tested and scraped due to projectiles jamming at high indexing speeds. Ultimately, an indexer with a spiral path was chosen to allow the indexing motor to reverse direction to clear jams
- High moment of inertia of the turret made tuning the yaw rotation difficult

<div class="post-content">
    <div class="image-row">
        <img src="{{ '/assets/img/IndexerPrototyping.png' | relative_url }}" alt="Early prototypes of the indexer" style="width: 40%; max-width: 40%;">
        <img src="{{ '/assets/img/Spiral_IndexerV2.png' | relative_url }}" alt="Final Duel Spiral Indexer Design" style="width: 30%; max-width: 30%;">
    </div>
</div>


**Background:**
[RoboMaster](https://www.robomaster.com/zh-CN) is an international robotics competition organized by the drone company DJI in which University teams design, build, and compete with ranged combat robots in an Esports style competition. Each robot must be built from the ground up integrating custom mechanical components, electronics, embedded controls, and high-level software such as computer vision.

One of the Robot types in RoboMaster is the Sentry, which must autonomously detect, engage, and fire upon the "armour plate" sensors on other robots. It features two 17mm barrels mounted on a turret which must be able to pitch, yaw, and direct plastic pellets towards targets.

<div class="post-content">
    <div class="image-row">
        <img src="{{ '/assets/img/Turret_Cross_Section2.png' | relative_url }}" alt="Turret Cross Section" style="width: 40%; max-width: 40%;">
        <img src="{{ '/assets/img/Solidworks_Sentry_2025.png' | relative_url }}" alt="Sentry in Solidworks" style="width: 50%; max-width: 50%;">
    </div>
</div>
Figures 2, 3: Final SOLIDWORKS 3D model of the Sentry turret and Cross section of the projectile path from the indexers to the flywheels