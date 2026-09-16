---
layout: post
title: Sip-and-puff fishing rod
date: 2024-04-06 00:00:00 -0700
description: Created the CAD and designed the electrical controls for a Sip-and-puff fishing rod to allow a Quadripeligic to go fishing # Add post description (optional)
img: SipNPuff_Render1.png # Add image post (optional)
tags: [Fusion 360, Arduino] # add tag
---

**Created the CAD and designed the electrical controls for a Sip-and-puff fishing rod for a Quadripeligic client**

<div class="post-content">
    <div class="image-row">
        <img src="{{ '/assets/img/Sip_and_Puff_Testing_Gif.gif' | relative_url }}" alt="Sip and puff fishing rod dry testing" style="width: 60%; max-width: 80%;">
        <img src="{{ '/assets/img/Sip_and_Puff_Electronics.png' | relative_url }}" alt="Sentry in Solidworks" style="width: 70%; max-width: 80%;">
    </div>
</div>
Figure 1: Sip and Puff fishing rod dry testing  
Figure 2: Internal electronics

**Results:**
- Uses an MPXV7002DP pressure sensor and joystick module to allow the user to cast, reel, lower, and raise the fishing rod with only their head.
- Two geared DC motors controls the movement of the fishing rod, both driven by a DB12 H-bridge
- The entire mechanism is controlled by an arduino uno powered through a voltage regulator

**Challenges and future improvements:**
- Casting speed limited by maximum motor rotation speed 
- Did not have time to implement a servo to actuate the bail
- A gooseneck should be added to ridgidly hold up the sip and puff mechanism
