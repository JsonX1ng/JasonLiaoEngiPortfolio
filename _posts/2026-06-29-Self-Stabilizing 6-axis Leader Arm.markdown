---
layout: post
title: Self-Stabilizing 6-axis Leader Arm
date: 2026-06-29 00:00:00 -0700
description: Coded, wrote the drivers for, and manufactured a self-stabilizing 6-axis leader arm  # Add post description (optional)
img: Engi_First_Block_Gif.gif # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [STM32, CAN bus, UART] # add tag
---
**Coded, wrote the drivers for, and manufactured a self-stabilizing 6-axis leader arm as a custom controller for my university team's "Engineer Robot"**

**Results:**
- Enabled the driver to control all 6 axes of the Engineer Robot's serial arm with one hand, providing an intuitive way to directly manipulate the robot's joints.
- Contributed to our team winning **2nd place** in the Engineer robot category at the 2026 [ARC Robotics Competition](https://www.arc-robotics.org/) in Purdue, Indiana.

<div class="post-content">
    <div class="image-row">
        <img src="{{ 'assets/img/Custom_Controller_2POVS_GIF.gif' | relative_url }}" alt="Testing the Custom Controller" style="width: 40%; max-width: 50%;">
        <img src="{{ 'assets/img/Custom_Controller_Self_Balancing_GIF.gif' | relative_url }}" alt="Showing the leader arm self-balancing" style="width: 34%; max-width: 50%;">
    </div>
</div>

**How:**
- Wrote a CAN bus driver library for the [K-Tech MS4005V3](https://lkmtech.en.alibaba.com/) mini servo motors, implementing the communication protocol to read motor position, set motor PID, and set motor velocity and torque.
- Implemented Free-RTOS tasks on the STM32 development board to read joint encoder positions, stabilize the wrist joints, and transmit commands via UART to the Robomaster Client.
- Designed adjustable counterweights on each link to balance the mass of the downstream links.
- Programmed a button and LED to calibrate the zero position of all the servo motors.

[**See the code for the leader arm custom controller here:**](https://github.com/JsonX1ng/ASN-Engineer-Custom-Controller)

**Challenges:**
- Debugged CAN communication issues caused by the mailbox buffer filling and dropping messages.
- Encountered a wrist-joint singularity in certain arm configurations that could cause one motor to rotate unexpectedly. This was fixed by adding addtional resisting torque to the preceding wrist motor.
- Implemented a watchdog to prevent undefined behaviour when the Robomaster Client timed out.

**Background:**
The "Engineer" robot is a specialized robot in the ARC (Formerly Robomaster North America) competition designed to manipulate field elements for points. This year, the goal of the competition was to grab and place large foam cubes into slots with random orientations. Our team achieved this with a Mecanum drive chassis equipped with a 6-axis robot arm featuring a suction-cup end effector.  
I designed the aforementioned 6-axis leader arm that mirrors the configuration of the robot's joints allowing the driver to manipulate the robot arm intuitively.