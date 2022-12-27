---
date: Nov 11, 2022
layout: post
title: The Meaning of Y-cap in Battery Electric Vehicles  
subtitle: Why Y-Cap is an important design factor?
description: Why Y-Cap is an important design factor?
image: /assets/img/Y_cap/Capacitors.jpg
category: Tech, EV
tags:
  - Tech
  - Engineering
  - EV
  - Electrification
author: abhijitdas
paginate: true
usemathjax: true
---
Y-capacitors and X-capacitors are common in the high voltage or traction voltage components of a battery electric vehicle (BEV). They are also present in the charging equipment. To understand why Y-cap and X-cap are needed, an understanding of different types noises is also needed. [Here](https://techweb.rohm.com/knowledge/emc/s-emc/01-s-emc/6899#:~:text=Common%20mode%20noise%20is%20noise,to%20the%20power%20supply%20line.) is a good article describing normal mode and common mode noises in a high-voltage system. A good overview of a traction voltage system (TVS), low voltage system (LVS), signal system (SS) normally present in any BEV are given below. 
### Traction Voltage System
In most cases, traction voltage system (TVS) is a floating system on top of the vehicle chassis where all high-voltage components are individually grounded to the chassis as shown in the figure below. In practice, designing a TVS for an EV is a little more complicated than what is seen in the figure. The following considerations are almost mandatory for safety, compatibility, packaging constraints, UN or local regulations.
- Size of the cables
- Length and routing of the cables
- Choice of connectors and its HVIL compatibility
- Size of Ground cables and their length
- Total Y-cap value for the whole vehicle (how about X-cap value?)

Separate blogs for each of the above items will follow.

| ![EV1](\assets\img\ElectricVehSteps\TVS_Arch3.png) |
|:--:|
| *This how a typical traction voltage topology would look like* |

### Low Voltage System
This part of the system is common between ICE vehicles and EV. Its getting common to have 24V or even 48V as low voltage (LV) system instead of widely used 12V system. Even though its possible to have a hybrid system where a few 12V system can co-exist if needed. We may consider CAN, ethernet and LIN nodes are part of LV topology. From the diagram below, I have also included a High Performance Unit/ECU (HPU) for computations like image processing and introducing adaptive Autosar architecture. A separate blog will follow on Adataptive Autosar at a later stage.

| ![EV2](\assets\img\ElectricVehSteps\LV_Arch.png) |
|:--:|
| *An example of a low voltage topology* |

### Physical Layout
Physical layout of high voltage and low voltage harness are as important as topology to manage packaging constraints as well as communication standards. For example, $J1939-11$ specifies a shielded twisted pair of wires with a maximum backbone length of $40$ meters. It uses a three pin connector and allows for up to $30$ nodes. It has a bit time of $4.00 \mu s$ with a tolerance of $0.05\%$.Some of the relevant links are given below -

[Overall EV related](https://www.motorvehicleregs.com/the_vehicle_reg_blog/electric-vehicles/)

[FMVSS standard](https://www.govinfo.gov/content/pkg/CFR-2017-title49-vol6/xml/CFR-2017-title49-vol6-part571.xml)

[j1939 physical layer](https://www.sae.org/standards/content/j1939/14_202204/)


| ![EV3](\assets\img\ElectricVehSteps\ev_batt.jpg) |
|:--:|
| *An electric battery pack on display at ACTExpo 2022* |
