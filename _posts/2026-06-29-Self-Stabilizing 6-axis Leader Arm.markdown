---
layout: post
title: Self-Stabilizing 6-axis Leader Arm
date: 2026-06-29 00:00:00 -0700
description: Coded, wrote the drivers for, and manufactured a self-stabilizing 6-axis leader arm  # Add post description (optional)
img: Custom_Controller_Pic.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [STM32, CAN bus, UART] # add tag
---
**Coded, wrote the drivers for, and manufactured a self-stabilizing 6-axis leader arm as a custom controller for my University team's "Engineer Robot"**

**Results:**
- Allowed the driver of the engineer robot to control all 6-axis of the serial robot arm with 1 hand in an intuitive way
- Led to our team winning **2nd place** for the Engineer robot category at the 2026 [ARC Robotics Competition](https://www.arc-robotics.org/) in Purdue, Indiana

<div class="post-content">
    <div class="image-row">
        <img src="{{ 'assets/img/Custom_Controller_2POVS_GIF.gif' | relative_url }}" alt="Testing the Custom Controller" style="width: 40%; max-width: 50%;">
        <img src="{{ 'assets/img/Custom_Controller_Self_Balancing_GIF.gif' | relative_url }}" alt="Showing the leader arm self-balancing" style="width: 34%; max-width: 50%;">
    </div>
</div>

**How:**
- Wrote a CAN bus driver library for the [K-Tech MS4005V3](https://www.robomaster.com/zh-CN) mini servo motors used in the design
- Implemented Free-RTOS tasks to read joint encoder positions, stabilize the wrist joints, and send the package via UART to the Robomaster Client
- Designed adjustable counterweights on each link to balance the mass of the subsequent links
- Programmed a button and LED to calibrate the 0 position of all the servo motors

**Challenges:**
- Encountered and debugged issues where the CAN bus mailbox buffer would fill up and drop messages
- Added a watchdog to prevent undefined behaviour when the Robomaster Client timed out

**Background:**
The "Engineer" robot is a specialized robot in the ARC (Formerly Robomaster North America) competition designed to manipulate field elements for points. This year, the goal of the competition was to grab and place large foam cubes into slots with random orientations. Our team achieved this with a Mecanum drive chassis equipped with with a 6-axis robot arm featuring a suction-cup end effector.  

I designed the aforementioned 6-axis leader arm to help control the joints of the robot mounted