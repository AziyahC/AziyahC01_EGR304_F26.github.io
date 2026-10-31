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

## Team Introduction & Member Roles

**Team 207** utilizes a hub-and-spoke architecture where specialized sensor boards transmit serial data to a central main processing board:
* **Aziyah Castellanoz (My Role) — Environmental Sensing & Hardware Engineer:** Designed and built the Temperature & Humidity Sensing Subsystem. Responsible for the DHT20 I²C digital sensor interface, 12V DC input to regulated +5V DC power supply, schematic capture, and transmitting serial temperature and humidity data over the 8-pin ribbon cable connector (J2) to the main board.

* **Dahryl Williams — Ambient Light Sensing Engineer:** Designed and built the Light Sensing Subsystem. Responsible for sampling ambient room light levels using a photo resistor circuit and sending the digitized light data serially to the central main board.

* **Chris Plumley — Central Hub & Actuator System Engineer:** Designed and built the Main Control & Actuator Board. Serves as the central hub that receives serial data from both my temperature/humidity sensor board and Dahryl's light sensor board. Because a traditional display screen was not compatible with our PIC Curiosity Nano setup, Chris's board uses this incoming sensor data to execute direct physical actions:
* **Temperature Actuation:** Automatically turns a cooling fan on or off depending on how hot or cold the room is based on readings from my DHT20 subsystem.
* **Lighting Actuation:** Dynamically adjusts the color array and brightness level of an ambient LED system based on light readings from Dahryl's photo resistor subsystem.

## Datasheet Navigation Guide
For visitors and reviewers navigating this datasheet, the documentation is organized into five specialized sections detailing each phase of the engineering design process:

* [01 Block Diagram](01-Block-Diagram/Block-Diagram.md): Shows the overall system layout, sensor connections, and how signal lines connect to the main board via the ribbon connector.

* [02 Component Selection](02-Component-Selection/Component-Selection.md): Review the engineering trade-off analysis, pros/cons, and rationale used to select major components, including the DHT20 sensor, L7805ABV-DG linear voltage regulator, and WSU120-0700 wall adapter.

* [03 Bill of Materials](03-BOM/BOM.md): Lists all physical components, costs, part numbers, vendor links, and schematic reference labels.

* [04 Schematic](04-Schematic/schematic.md): Inspect the full KiCad ECAD circuit schematic, functional sub-block breakdowns (Power Regulation, MCU Core, Sensing, Communication, UI, and Test Points).

* [05 Power Budget](05-Power-Budget/Power-Budget.md): Breaks down power consumption, current draw across operating modes, and power supply efficiency.

For all the sections
