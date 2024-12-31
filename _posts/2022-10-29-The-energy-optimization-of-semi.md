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
highlight: true
tags:
  - Tech
  - Engineering
  - EV
  - Electrification
author: abhijitdas
paginate: true
usemathjax: true
---
Electric vehicles, especially cars, have become more common recently. Inspired by Tesla’s success, many new startups are emerging. It’s not just cars—there are also heavy-duty trucks, material handling equipment, boats, construction, and agricultural machines. However, range anxiety is still a concern for many OEMs.

One reason for this anxiety is that battery technology hasn’t seen any major breakthroughs recently. This limits significant range improvements with the current battery sizes. Instead, improving energy efficiency could be the key to extending the range of BEV trucks. Some factors for improving energy efficiency are similar to those in diesel trucks, but others are unique to electric vehicles. Here are some key contributors:

### Aerodynamics

Aerodynamics plays a big role in energy consumption because of drag. The diagram below from STEMCO shows how the tractor and trailer contribute to the overall drag of a heavy-duty truck.

| ![EV2](\assets\img\ElectricVehSteps\Stemco-contributions-to-semi-aero-drag.png) |
|:--:|
| *Distribution of aerodynamic drag between tractor and trailer (STEMCO)* |

Efforts are ongoing to reduce drag by redesigning trucks. For example, Tesla’s Semi has a sleek design that may reduce air drag compared to conventional trucks. The report from [Airshaper](https://airshaper.com/cases/tesla-semi-truck-aerodynamics-analyzed) below shows this comparison.

| ![EV3](\assets\img\ElectricVehSteps\tesla_semi_aero.png) |
|:--:|
| *Tesla Semi vs. conventional truck (Airshaper)* |

Projects like the DOE-funded SuperTruck also focus on reducing drag. A [report](https://lynceans.org/tag/truck-aerodynamics/) by the Lyncean Group of San Diego highlights these efforts. Additionally, technologies like the [Sinha Deturbulator](http://sinhatech.com/Sinhadeturb/deturbulator.asp) are worth mentioning.

| ![EV4](\assets\img\ElectricVehSteps\Sinha_deturbulator.jpg) |
|:--:|
| *The deturbulator by Sinhatech could reduce aerodynamic drag losses* |

### Axial Flux Motors

Axial flux motors are less common but highly efficient. These motors, a type of permanent magnet synchronous motor (PMSM), offer better efficiency and space-saving benefits than radial flux motors. They’re especially useful for auxiliary systems that run continuously in trucks. Below is a comparison shared by Yasa, a leading axial flux motor manufacturer.

| ![EV5](\assets\img\ElectricVehSteps\Yasa_Axial_Flux_Motor.jpg) |
|:--:|
| *Comparison of axial and radial flux motors (Yasa)* |

For more on axial flux motors, you can read this [PhD thesis](https://web.mit.edu/kirtley/binlustuff/literature/electric%20machine/designOfAxialFluxPMM.pdf) or this simpler [article](https://spectrum.ieee.org/axial-flux-motor#toggle-gdpr) (requires IEEE membership).

Yasa, now owned by Mercedes-Benz, is set to produce axial flux motors for its products ([source](https://www.greencarcongress.com/2021/11/20211119-yasa.html)). Another manufacturer, [Omni Powertrain Technologies](https://www.omnipowertrain.com/), offers motors ranging from 3 kW to 192 kW ([brochure](https://www.omnipowertrain.com/wp-content/uploads/2022/02/Magelec-Propulsion-Brochure.pdf)).

Though not yet widely adopted, axial flux motors show promise for improving efficiency in heavy-duty trucks.

### Recuperation of Braking Energy

Braking energy recovery is crucial for improving efficiency. On certain US highways, trucks may descend continuously for hundreds of miles ([elevation map](https://www.reddit.com/r/Truckers/comments/kafeg1/elevation_map_of_the_us_interstate_system/)).

| ![EV6](\assets\img\ElectricVehSteps\US_interstate_elevation.jpeg) |
|:--:|
| *Elevation map of US interstate system ([source](https://i.imgur.com/72ziOLR.jpg))* |

Currently, OEMs use brake resistors to dissipate excess braking energy as heat. While this reduces wear on service brakes, it doesn’t improve efficiency.

| ![EV7](\assets\img\ElectricVehSteps\Brake_Resistor.jpg) |
|:--:|
| *Typical brake resistor used for braking (REPLLC)* |

### Tires

Like aerodynamics, rolling resistance also affects efficiency. This [article](https://www.fleetequipmentmag.com/fuel-efficiency-heavy-duty-truck-tires/) explains how tires impact performance. Michelin’s *X One* tires, for example, claim to reduce rolling resistance.

| ![EV6](\assets\img\ElectricVehSteps\Tire_truck.jpg) |
|:--:|
| *Tires play a crucial role in energy efficiency* |

| ![EV7](\assets\img\ElectricVehSteps\michelin_tire.png) |
|:--:|
| *Energy loss distribution around trucks and trailers* |

### Conclusion and Tesla Semi Example

While aerodynamics and rolling resistance are being addressed, there’s still room to improve braking energy recovery and adopt axial flux motors. For instance, during Tesla Semi’s 500-mile test in late 2022, it recovered 16% of the battery energy while descending from 4136 ft to 1000 ft after using 28% of energy to climb the same elevation.

| ![EV8](\assets\img\ElectricVehSteps\Tesla_semi_batt_discharge_graph.png) |
|:--:|
| *Potential for improving energy recovery* |

Below are calculations showing only 49% of the potential energy was recovered during the descent.

| Parameter/Variable                       | Value     | Unit  |
| ---------------------------------------- | --------- | ----- |
| Mass                                     | 37200     | kg    |
| g                                        | 9.81      | m/s^2 |
| Elevation                                | 955       | Meter |
| Batt Capacity                            | 990       | kWh   |
| Max Potential Energy                     | 348.5     | MJ    |
| Energy Recovered                         | 178.2     | MJ    |
| Recuperation Efficiency                  | 49%       | %     |

| ![EV9](\assets\img\ElectricVehSteps\Braking_calc.png) |
|:--:|
| *Energy conservation in braking* |

Based on these numbers, brake resistors or other energy dissipators remain essential for safety, especially on steep descents. They help manage braking energy when the battery system cannot store it.

| ![EV10](\assets\img\ElectricVehSteps\brake_energy_table.jpg) |
|:--:|
| *Brake energy calculations for the descent* |

