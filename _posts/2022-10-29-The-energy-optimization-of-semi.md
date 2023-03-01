---
date: May 01, 2022
layout: post
title: Energy Optimization for Battery Electric Heavy Duty Trucks  
subtitle: Areas where energy efficiency can be improved or optimized
description: Areas where energy efficiency can be improved or optimized
image: /assets/img/ElectricVehSteps/Volvo_eVNR_homepage_3.png
optimized_image: /assets/img/ElectricVehSteps/ev_optimized.jpg
description: Why electric vehicles are not less complicated than ICE ones.
image: /assets/img/ElectricVehSteps/Volvo_eVNR_homepage_3.png
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
Electrics Vehicles especially cars are becoming common in recent times. Inspired by Tesla's success, a lot of new start-ups are coming up everywhere. It's just not the cars, but also heavy-duty trucks, material handling, boat and construction and agricultural machines. Although the range anxiety is still quite visible among the OEMs. One of the main reasons for the persisting range anxiety lies in the fact that in the last few years the battery technology doesn't have any path-breaking innovation to provide a significant range improvement given the fixed size of the battery pack. Therefore, finding a way to improve energy efficiency instead could be the way to improve the existing range for BEV trucks. Some of the elements behind improving energy efficiency for BEV trucks are the same as Diesel trucks but some of them are unique. Here are some relevant contributors - 

### Aerodynamics
Aerodynamics plays an important role in energy consumption due to drag. The figure below by STEMCO shows how the combination of tractor and trailer contributes to the overall energy efficiency of a heavy-duty truck. 

| ![EV2](\assets\img\ElectricVehSteps\Stemco-contributions-to-semi-aero-drag.png) |
|:--:|
| *Distribution of aerodag between tractor and trailer (STEMCO)* |

There are ongoing efforts to minimize the effect of drag on trucks by redesigning external long nosy cabs into something that a Tesla Semi is offering. See below a report published by [Airshaper](https://airshaper.com/cases/tesla-semi-truck-aerodynamics-analyzed) which shows that Tesla's semi design may be benefitting from reduced air drag in comparison to its competitors. 

| ![EV3](\assets\img\ElectricVehSteps\tesla_semi_aero.png) |
|:--:|
| *Tesla Semi vs Conventional Truck (Airshaper)* |

In addition, DOE funded super truck project also unvails the effort by OEMs like Volvo, etc. to overcome the so-called drag difficulties. A [report](https://lynceans.org/tag/truck-aerodynamics/) published by Lyncean Group of San Diego nicely summarized this effort. 

The technologies like [Sinha Deturbulator](http://sinhatech.com/Sinhadeturb/deturbulator.asp) would also be worth the mention. 

| ![EV4](\assets\img\ElectricVehSteps\Sinha_deturbulator.jpg) |
|:--:|
| *The deturbulator by Sinhatech could contribute to redeuce loss due to aero drag* |

### Axial flux motors
Axial flux motors are still not visible to many. Electric motors or machines especially permanent magnet synchronous motors (PMSM) are highly efficient when controlled properly. Axial flux motors are a type of PMSM motor that offer even more efficiency and packaging benefits compared to radial flux motors. Auxiliaries that run all the time irrespective of the movement of the truck itself, would certainly benefit from using axial flux technology. Yasa, an axial flux motor manufacturer, demonstrated the benefits below - 

| ![EV5](\assets\img\ElectricVehSteps\Yasa_Axial_Flux_Motor.jpg) |
|:--:|
| *A comparision study between axial and radial flux motors (Yasa)* |

[Here](https://web.mit.edu/kirtley/binlustuff/literature/electric%20machine/designOfAxialFluxPMM.pdf) is a good PhD theis if you would like to know more about axial flux motor design. If you dont want to get into too much technical details, [this](https://spectrum.ieee.org/axial-flux-motor#toggle-gdpr) article would be for you (Requires IEEE membership to view). 

Yasa is now owned by Marcedes-Benz and will do serial production of axial flux motors for its products [Ref](https://www.greencarcongress.com/2021/11/20211119-yasa.html). The other notable axial flux motor manufacturer is [Omni Powertrain Technologies](https://www.omnipowertrain.com/). Omni claims to have axial flux motors ranging from 3.0kW to 192kW (dual motors) in its portfolio [Ref](https://www.omnipowertrain.com/wp-content/uploads/2022/02/Magelec-Propulsion-Brochure.pdf).

As mentioned earlier, axial flux technology is yet to earn trust globally, but based on the fact available from early adopters and manufacturers, it could play an important role in EV's overall energy efficiency, especially for heavy-duty trucks where there are several auxiliaries are used. 

### Recuperation of braking energy 

This is the most important aspect of energy optimization that has a good scope for improvement. Today, the braking energy must go wasted if not going back to the energy storage system (ESS). If we analyze the US highway overall topography for usual truck routes, it is evident that in some cases the truck has to go downhill continuously for more than hundreds of miles (based on the [map](https://www.reddit.com/r/Truckers/comments/kafeg1/elevation_map_of_the_us_interstate_system/) shared by a Reddit user). For battery electric trucks, ESS would not be able to take all the braking energy back in those routes and must find another way to recuperate. 

| ![EV6](\assets\img\ElectricVehSteps\US_interstate_elevation.jpeg) |
|:--:|
| *Elevation map of the US interstate system ([Source](https://i.imgur.com/72ziOLR.jpg))* |

As of today, OEMs are mostly using brake resistor to discard the extra braking energy as heat. Note that, even after careful sizing, a brake resistor often needs an elaborate cooling system which sometimes causes a packaging nightmare. In addition, brake resistor may expand the lifespan of the service brakes but does not contribute to the energy efficiency. 

| ![EV7](\assets\img\ElectricVehSteps\Brake_Resistor.jpg) |
|:--:|
| *A typical Brake sistor used for braking (REPLLC))* |

### Tires

Simialr to aerodynamics, rolling resistance is also a contributing factor to efficiency. This [article](https://www.fleetequipmentmag.com/fuel-efficiency-heavy-duty-truck-tires/) nicely summarizes the effect of tires on efficiency. Tire manufacturers like [Michelin](https://business.michelinman.com/fuelsaver) already have products like *X One* that claims to reduce rolling resistance for trucks and trailers. 

| ![EV6](\assets\img\ElectricVehSteps\Tire_truck.jpg) |
|:--:|
| *Tires play an important role to energy efficiency* |

| ![EV7](\assets\img\ElectricVehSteps\michelin_tire.png) |
|:--:|
| *Division of energy losses around trucks and trailers* |

### Conclusion and Tesla Semi example
Although there is work in progress for improving aerodynamics and rolling resistance, there are a lot of attention is needed for other contributors like recuperation of braking energy and using axial flux motor technologies. Here is another fun fact based on Tesla Semi's 500-mile run in late 2022. As shown in the image below, it recovered about 16% battery energy to come back to an elevation of 1000 ft from 4136 ft where it utilized 28% of battery energy to climb the same height. Yes, there are some assumptions in these numbers, but there might be an opportunity hiding to improve the recuperation beyond 16%. In addition, based on my calculation below (table), only 49% of the total potential energy were recovered.  

| ![EV8](\assets\img\ElectricVehSteps\Tesla_semi_batt_discharge_graph.png) |
|:--:|
| *Potential opportunity for range improvement* |

| Based on the Graph right hand side | Positions Miles | SOC   | % Change | Absolute change |
| ---------------------------------- | --------------- | ----- | -------- | --------------- |
| Pt A                               | 267.99          | 46.29 |     ~    |     ~           |
| Pt B                               | 280.90          | 33.12 | \-28%    | \-13.2          |
| Pt C                               | 311.35          | 38.43 | 16%      | 5.3             |


| Parameter/Variable                       | Value     | Unit  |
| ---------------------------------------- | --------- | ----- |
| Mass                                     | 37200     | kg    |
| g                                        | 9.81      | m/s^2 |
| Elevation                                | 955       | Meter |
| ---------------------------------------- | --------- | ----- |
| Batt Capacity                            | 990       | kwhr  |
| Batt Capacity                            | 3564      | MJ    |
| ---------------------------------------- | --------- | ----- |
| Max Potential Energy in Joule            | 348510060 | J     |
| Max Potential Energy in MJ               | 348.5     | MJ    |
| Energy used to cover 955 meter elevation | 470.448   | MJ    |
| ---------------------------------------- | --------- | ----- |
| DOD at the highest point                 | 2387.88   | MJ    |
| Energy recovered                         | 178.2     | MJ    |
| ---------------------------------------- | --------- | ----- |
| Energy Recuperation Efficiency           | 49%       |  %    |

| ![EV9](\assets\img\ElectricVehSteps\Braking_calc.png) |
|:--:|
| *The Conservation of Energy for braking* |

The code for the calculation is given below - 
```python
fun test_me():
    print('yes, backticks work!')
```
```python
from math import sin, cos, tan
from sympy import symbols, solve
batt_cap = 3564 # MJ
m = 37200 # kg
g = 9.81 # m/s^2
# At Pt A
h1 = 955 # meter
v1 = 0 # m/s
########################################################################################################################
# At pt B
v2 = 26.67 #m/s
theta = 0.02 # rad
cd = 0.36
A = 9.87 # m^2
crr = 0.005
eta = 0.95
rho = 1.2 # kg/m^3
h2 = symbols('h2')
l1 = symbols('l1')
########################################################################################################################
expr1 = m*g*l1*sin(theta) - 0.5*m*v2**2 - crr*m*g*cos(theta)*l1 - 0.5*cd*rho*A*v2**2*l1
l1 = solve(expr1)
l1 = l1[0]
print('l1 = ', round(l1, 2))
expr2 = h1 - h2 - l1*sin(theta)
h2 = solve(expr2)
h2=h2[0]
print('h2 = ', round(h2, 2)) 
l = (311 - 280)*1609 # meter
l2 = l - l1 # meter
h2 = 888.14 # meter
W_fr_l2 = crr*m*g*cos(theta)*l2 # work done to compensate friction to cover the distacne l2
W_aero_l2 = 0.5*cd*rho*A*v2**2*l2 # work done to compensate aero resistance to cover the distacne l2 assming a constant speed of 60 miles/hr
E_pe_h2 = m*g*h2 # Potential energy at point B
E_tot_loss = W_fr_l2 + W_aero_l2 # total loss for travelling l2 distance
E_braking = E_pe_h2 - E_tot_loss # Energy that needs to go to Battery to maintian constat speed of 60 mph
E_battery_remaining = 0.35*batt_cap - E_braking/1e6 # Remaining batt capacity
########################################################################################################################
print('Max allowed speed = ', v2, 'm/s')
print('Max elevation = ', h1, 'meter')
print('Total travelled distance = ', l, 'meter')
print('The elevation at which the speed will reach 60mph = ', round(h2, 2), 'meter')
print('The distance at which the speed will reach 60mph = ', round(l1,2), 'meter')
print('Work done to compensate friction to cover the distacne l2 = ', round(W_fr_l2,2), 'joules or =', round(W_fr_l2/1e6, 2), 'MJ')
print('Work done to compensate aero resistance to cover the distacne l2 assming a constant speed of 60 miles/hr = ', round(W_aero_l2, 2), 'joules or =', round(W_aero_l2/1e6,2), 'MJ')
print('Total energy loss due to travelling l2 distance =', round(E_tot_loss, 2), 'joules or =', round(E_tot_loss/1e6,2), 'MJ')
print('Potential energy at point B = ', round(E_pe_h2,2), 'joules or =', round(E_pe_h2/1e6,2), 'MJ')
print('Energy that needs to go to Battery to maintian constat speed of 60 mph = ', round(E_retarder,2), 'joules or =', round(E_retarder/1e6,2), 'MJ')
print('Remianing Batt Energy = ', round(E_battery_remaining,2), 'MJ')
```