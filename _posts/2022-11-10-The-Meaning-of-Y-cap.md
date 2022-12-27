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
Y-capacitors and X-capacitors are common in the high voltage or traction voltage components of a battery electric vehicle (BEV). They are also present in the charging equipment. To understand why Y-cap and X-cap are needed, an understanding of different types of noises is also needed. [Here](https://techweb.rohm.com/knowledge/emc/s-emc/01-s-emc/6899#:~:text=Common%20mode%20noise%20is%20noise,to%20the%20power%20supply%20line.) is a good article describing normal mode and common mode noises in a high-voltage system. If you are not already familiar, a rough overview of a high/traction voltage system (TVS), low voltage system (LVS), and signal system (SS) normally present in any BEV is given at the end. The types of safety capacitors (X-cap and Y-cap) and their usage is described in this [article](https://recom-power.com/en/rec-n-class-x-and-class-y-safety-capacitors-142.html?0). The use of X-cap and Y-cap on ESS is discussed in this [article](https://blog.knowlescapacitors.com/blog/looking-closer-at-filter-capacitors-in-electric-vehicles). For EV, Y-cap is more relevant as TVS is mostly comprised of DC bus lines. Most of the components including the energy storage system (ESS) and Auxiliaries have one or more Y-cap(s). While charging through electric vehicle supply equipment (EVSE), these capacitors consume a discrete amount of energy before ESS starts charging. Therefore, the amount of stored energy depends on the overall Y-cap of the vehicle. Based on the regulation, a vehicle can not store more than 0.1 joules of energy at a given time. So, the total Y-cap value of a vehicle has to be limited to a certain value to pass the regulation. On the other hand, during charging, if the charge goes to Y-cap first, EVSE will detect a delay/anomaly in response from ESS based on the given power output from the EVSE. In most cases, EVSE is aware of the presence of Y-cap in EV. But if the Y-cap value, goes beyond the regulated value, then EVSE would raise a fault and stop charging. This is why having too many high-voltage components in a BEV vehicle may cause charging issues. The graph below (Source: [Sendyne](https://www.sendyne.com/Company/Publications/Capacitance%20hazards%20in%20e-mobility%20v0.1.pdf) shows the regulated value of Y-cap in a BEV. 

| ![EV1](\assets\img\Y_cap\capacitance_limit.png) |
|:--:|
| *Capacitance limit vs Voltage. The blue line corresponds to the 0.2 Joules limit imposed by several standards. The range of applicability of the Fq based limit starts at 240 V (Source: Sendyne)* |

Therefore, Y-cap value not only depends on the number of high voltage components on-board, but also the traction voltage value. In general, the Y-cap value can be obtained from the supplier through technical documentation. Then, based on the connection of that component to the rest of the system like series or parallel, an overall value for Y-cap can be obtained for the overall system. 

| ![EV2](\assets\img\Y_cap\ycap_voltage_limits_regulation.png) |
|:--:|
| *Capacitance limit also depends on voltage. All revenat regulations related to Y-cap for EV* | 

As shown in the TVS topology (next stection), high voltage components in EV are supplied through a single traction voltage power distribution system (TVPDC) so, the Y-caps for those components are always stay in parralel and thus contribute directly to the increase of the overall Y-cap rise of the system. 

| ![EV2](\assets\img\Y_cap\Capacitor_in_parallel.png) |
|:--:|
| *Capacitors in parallel means overall capacitance value will increase* | 

To solve the charging issue due to high Y-cap, seems like [Sendyne](https://www.sendyne.com/Company/Publications/Capacitance%20hazards%20in%20e-mobility%20v0.1.pdf) is working to dynamically measure Y-cap value for EV. In that case, EVSE can take more informed decision before interrupt a charging session due to delay in response from EV. But satisfying the regulation to limit the total energy stored at a given time in an EV would still be a challange. 

### Traction Voltage System
In most cases, traction voltage system (TVS) is a floating system on top of the vehicle chassis where all high-voltage components are individually grounded to the chassis as shown in the figure below. In practice, designing a TVS for an EV is a little more complicated than what is seen in the figure. The following considerations are almost mandatory for safety, compatibility, packaging constraints, UN or local regulations.
- Size of the cables
- Length and routing of the cables
- Choice of connectors and its HVIL compatibility
- Size of Ground cables and their length
- Total Y-cap value for the whole vehicle (discussed above)

Separate blogs for each of the above items will follow.

| ![EV3](\assets\img\ElectricVehSteps\TVS_Arch3.png) |
|:--:|
| *This how a typical traction voltage topology would look like* |

### Low Voltage System
This part of the system is common between ICE vehicles and EV. Its getting common to have 24V or even 48V as low voltage (LV) system instead of widely used 12V system. Even though its possible to have a hybrid system where a few 12V system can co-exist if needed. We may consider CAN, ethernet and LIN nodes are part of LV topology. From the diagram below, I have also included a High Performance Unit/ECU (HPU) for computations like image processing and introducing adaptive Autosar architecture. A separate blog will follow on Adataptive Autosar at a later stage.

| ![EV4](\assets\img\ElectricVehSteps\LV_Arch.png) |
|:--:|
| *An example of a low voltage topology* |

### Physical Layout
Physical layout of high voltage and low voltage harness are as important as topology to manage packaging constraints as well as communication standards. For example, $J1939-11$ specifies a shielded twisted pair of wires with a maximum backbone length of $40$ meters. It uses a three pin connector and allows for up to $30$ nodes. It has a bit time of $4.00 \mu s$ with a tolerance of $0.05\%$.Some of the relevant links are given below -

[Overall EV related](https://www.motorvehicleregs.com/the_vehicle_reg_blog/electric-vehicles/)

[FMVSS standard](https://www.govinfo.gov/content/pkg/CFR-2017-title49-vol6/xml/CFR-2017-title49-vol6-part571.xml)

[j1939 physical layer](https://www.sae.org/standards/content/j1939/14_202204/)


| ![EV5](\assets\img\ElectricVehSteps\ev_batt.jpg) |
|:--:|
| *An electric battery pack on display at ACTExpo 2022* |
