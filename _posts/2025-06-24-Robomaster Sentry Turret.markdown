---
layout: post
title: Robomaster Sentry Turret
date: 2025-06-24 00:00:00 -0700
description: I Designed and manufactured the turret of our University team's Sentry Robot for the 2025 Robomaster North America (RMNA) Robotics Competition. # Add post description (optional)
img: Sentry2025.jpeg # Add image post (optional)
tags: [Solidworks, 3DPrinting, Waterjet, DFM] # add tag
---
**I Designed and manufactured the turret of our University team's Sentry Robot for the 2025 Robomaster North America (RMNA) Robotics Competition.**
 
<div class="post-content">
    <div class="image-row">
        <img src="{{ '/assets/img/Solidworks_Sentry_2025.png' | relative_url }}" alt="Turret Cross Section" style="width: 40%; max-width: 50%;">
        <img src="{{ '/assets/img/Turret_Cross_Section2.png' | relative_url }}" alt="Sentry in Solidworks" style="width: 36%; max-width: 50%;">
    </div>
</div>
Figure 1: Final SOLIDWORKS 3D model of the Sentry turret  
Figure 2: Cross section of the projectile path from the indexers to the flywheels

**Results:**
- Capable of indexing and firing at 1500 rounds per minute at targets
- Achieves Pitch and Yaw aim control with 2 BLDC motors
- Final construction made from waterjet-cut fibreglass composite plates and 3D printed PPA-CF
- Electrically connects to the chassis through a pogo pin PCB

<div class="post-content">
    <div class="image-row">
        <img src="{{ '/assets/img/Sentry_Assesment_2025_gif.gif' | relative_url }}" alt="Firing test for a 3D printed prototype of the Sentry" style="width: 70%; max-width: 70%;">
        <img src="{{ 'assets/img/Sentry_Tracking_Tuning_Gif.gif' | relative_url }}" alt="Tuning the Sentry Tracking" style="width: 22%; max-width: 30%;">
    </div>
</div>
Figure 3: Firing test for a 3D printed prototype of the Sentry for the 2025 technical assessment  
Figure 4: Tuning the Sentry's tracking of other robot's armous plate

**Challenges:**
- Many, many indexer iterations were tested and scraped due to projectiles jamming at high indexing speeds. Ultimately, an indexer with a spiral path was chosen to allow the indexing motor to reverse direction to clear jams
- Stacking the ammo hopper above the mainboard enclosure made electrical maintainence difficult at times
- The turret's high moment of inertia made tuning the yaw rotation difficult
- When the firing flywheels spin up, the centripedal force expands them slightly, risking contact with a nearby cable, additional cable trays had to be added


<div class="post-content">
    <div class="image-row">
        <img src="{{ '/assets/img/Indexer_Testing_Gif.gif' | relative_url }}" alt="Testing early prototypes of the indexer" style="width: 55%; max-width: 60%;">
        <img src="{{ '/assets/img/Spiral_IndexerV2.png' | relative_url }}" alt="Final Duel Spiral Indexer Design" style="width: 35%; max-width: 40%;">
    </div>
</div>
Figure 5: Indexing test for an early prototype of the indexer. Jams would often occur requiring adjustments to tolerances and small sections of geometry  
Figure 6: Final Duel Spiral Indexer Design (Derived from a design by Liang Nie)


**Background:**  
[RoboMaster](https://www.robomaster.com/zh-CN) is an international robotics competition organized by the drone company DJI in which University teams design, build, and compete with ranged combat robots in an Esports style competition. Each robot must be built from the ground up integrating custom mechanical components, electronics, embedded controls, and high-level software such as computer vision.

One of the Robot types in RoboMaster is the Sentry, which must autonomously detect, engage, and fire upon the "armour plate" sensors on other robots. It features two 17mm barrels mounted on a turret which must be able to pitch, yaw, and direct plastic pellets towards targets.