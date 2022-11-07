---
date: May 01, 2022
layout: post
title: What is in an electric vehicle?
subtitle: A few simplified steps
description: Why electric vehicles are not less complicated than ICE ones.
image: /assets/img/ElectricVehSteps/ev_bus.jpg
optimized_image: /assets/img/ElectricVehSteps/ev_optimized.jpg
category: Tech
tags:
  - Tech
  - Engineering
  - EV
  - Electrification
author: abhijitdas
paginate: true
---
Still in progress....

Electrics Vehicles especially cars are becoming common in recent times. Inspired by Tesla's success, a lot of new start-ups are coming up everywhere. It's just not the cars, but also trucks or tractors, forklifts, boat and construction and agricultural machines. Based on the recent success of the EV start-ups, it's evident that building an one of prototype car is not the same as developing and building a process to produce hundreds of cars per month. Because the adaptation to traction voltage system hasn't matured yet, it's still a complicated process overall to build a production quality EV while taking into account energy efficiency, charging performance, various regulations, cyber security, safety of traction voltage related components and cables, grounding etc. Here are some of the aspects that I think would be important to mention.

**Traction Voltage System**
In most cases TVS is floating system on top of the vehicle chassis where all high voltage components are individually grounded to chassis as shown in the figure below. In practical, designing a TVS for a EV is a little more complicated than what is seen in the figure. The following considerations are almost mandatory for safety, compatibility, packaging constraints, UN or local regulations.
1. Size of the cables
2. Length and routing of the cables
3. Choice of connectors and its HVIL compatibility
4. Size of Ground cables and their length
5. Total Y-cap value for the whole vehicle (how about X-cap value?)
Separate blogs for each of the above items will follow.
![An example of a TVS Topology](\assets\img\ElectricVehSteps\TVS_Arch2.png)

**Low Voltage System**
This part of the system is common between ICE vehicles and EV. Its getting common to have 24V or even 48V as low voltage (LV) system instead of widely used 12V system. Even though its possible to have a hybrid system where a few 12V system can co-exist if needed. We may consider CAN, ethernet and LIN nodes are part of LV topology. From the diagram below, I have also included a High Performance Unit/ECU (HPU) for computations like image processing and introducing adaptive Autosar architecture. A separate blog will follow on Adataptive Autosar at a later stage.   
![An example of a LV Topology](\assets\img\ElectricVehSteps\LV_Arch.png)

![An electric battery pack on display at ACTExpo 2022](\assets\img\ElectricVehSteps\ev_batt.jpg)
