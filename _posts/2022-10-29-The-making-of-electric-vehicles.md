---
date: May 01, 2022
layout: post
title: The Making of Energy Optimized Battery Electric Heavy Duty Trucks  
subtitle: A $360^\circ$ approach
description: Why electric vehicles are not less complicated than ICE ones.
image: /assets/img/ElectricVehSteps/ev_bus.jpg
optimized_image: /assets/img/ElectricVehSteps/Volvo_eVNR_homepage_3.png
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
In Progress ---
Electrics Vehicles especially cars are becoming common in recent times. Inspired by Tesla's success, a lot of new start-ups are coming up everywhere. It's just not the cars, but also trucks or tractors, forklifts, boat and construction and agricultural machines. Based on the recent success of the EV start-ups, it's evident that building an one of prototype car is not the same as developing and building a process to produce hundreds of cars per month. Because the adaptation to traction voltage system hasn't matured yet, it's still a complicated process overall to build a production quality EV while taking into account energy efficiency, charging performance, various regulations, cyber security, safety of traction voltage related components and cables, grounding etc. Here are some of the aspects that I think would be important to mention.

**Traction Voltage System**
In most cases TVS is floating system on top of the vehicle chassis where all high voltage components are individually grounded to chassis as shown in the figure below. In practical, designing a TVS for a EV is a little more complicated than what is seen in the figure. The following considerations are almost mandatory for safety, compatibility, packaging constraints, UN or local regulations.
- Size of the cables
- Length and routing of the cables
- Choice of connectors and its HVIL compatibility
- Size of Ground cables and their length
- Total Y-cap value for the whole vehicle (how about X-cap value?)

Separate blogs for each of the above items will follow.

| ![EV1](\assets\img\ElectricVehSteps\TVS_Arch2.png) |
|:--:|
| *This how a typical traction voltage topology would look like* |

**Low Voltage System**
This part of the system is common between ICE vehicles and EV. Its getting common to have 24V or even 48V as low voltage (LV) system instead of widely used 12V system. Even though its possible to have a hybrid system where a few 12V system can co-exist if needed. We may consider CAN, ethernet and LIN nodes are part of LV topology. From the diagram below, I have also included a High Performance Unit/ECU (HPU) for computations like image processing and introducing adaptive Autosar architecture. A separate blog will follow on Adataptive Autosar at a later stage.

| ![EV1](\assets\img\ElectricVehSteps\LV_Arch.png) |
|:--:|
| *An example of a low voltage topology* |

**Physical Layout**
Physical layout of high voltage and low voltage harness are as important as topology to manage packaging constraints as well as communication standards. For example, $J1939-11$ specifies a shielded twisted pair of wires with a maximum backbone length of $40$ meters. It uses a three pin connector and allows for up to $30$ nodes. It has a bit time of $4.00 \mu s$ with a tolerance of $0.05\%$.Some of the relevant links are given below -

[Overall EV related](https://www.motorvehicleregs.com/the_vehicle_reg_blog/electric-vehicles/)

[FMVSS standard](https://www.govinfo.gov/content/pkg/CFR-2017-title49-vol6/xml/CFR-2017-title49-vol6-part571.xml)

[j1939 physical layer](https://www.sae.org/standards/content/j1939/14_202204/)


| ![EV1](\assets\img\ElectricVehSteps\ev_batt.jpg) |
|:--:|
| *An electric battery pack on display at ACTExpo 2022* |
