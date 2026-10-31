---
title: Welcome
tags:
- tag1
- tag2
---
<center>
<font size= "6">Aziyah Castellanoz Datasheet</font><br>
as part of <br>
<font size= "8"> Robots</font><br>
for<br>
<font size= "5"> Team 207 </font><br>

**Submission: October , 30, 2026**
</center>

## Introduction

Welcome to the technical data sheet for the Temperature & Humidity Sensing Subsystem. The purpose of this datasheet is to serve as a comprehensive, standalone engineering documentation hub for the electrical design, component selection, schematic capture, power analysis, and hardware specification of this embedded subsystem. Designed as part of ASU's EGR 304 course, this data sheet provides all necessary technical details, schematic diagrams, and bill-of-materials data required to build, interface, and verify the physical hardware.

### Project Summary

The Dorm Hub project is a compact, multi-functional desktop environmental monitor and smart ambient light sensing tailored specifically for university students living in ASU dormitories. Dorm rooms present unique challenges—limited living space, fluctuating room climates, and busy student schedules. The Dorm Hub solves these issues by consolidating ambient lighting, sleep/wake routines, and real-time climate monitoring into a single space-saving desktop device.

### My Contribution

As my individual engineering contribution to Team 207, I designed and implemented the Temperature & Humidity Sensing Subsystem. This module acts as the environmental intelligence unit for the Dorm Hub, continuously sampling ambient room temperature (–40°C to 80°C) and relative humidity (0–100% RH) via an Adafruit DHT20 digital sensor over an I²C serial bus.

The onboard Microchip PIC18F57Q43 Curiosity Nano microcontroller processes the digital sensor readings and communicates with the rest of the team's modules over a standardized 8-pin shrouded ribbon cable interface. This allows my teammates' display and control subsystems to dynamically adjust room settings, display live weather/room metrics, and trigger environmental alerts.

To examine how this subsystem integrates into Team 207's overall hub-and-spoke hardware architecture, software state machine, and complete product requirements, please visit the main [Team 207 Project Report](https://asu-egr304-2026-f-207.github.io/TEAM207_EGR304-FALL_2026/)

* [Component Selection](02-Component-Selection/Component-Selection.md)





* This needs to be updated to reflect a team introduction
* Content should also help an unfamiliar reader navigate to areas of interest. Information like:

To review the details listed of the material used to construct the subsection, you can review it in the ["BOM"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/03-BOM/BOM/) section of the datasheet.

For all the sections
