---
title: Bill of Materials
tags:
- tag1
- tag2
---

## Overview
written context

## Bill of Materials Example (as Table)

*Table ##: An example of one approach to adding your BOM table to this section.*

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
8-bit SIPO/SISO Shift Register, SOIC-16 package | 1 | $0.49 | $ 0.49 | NXP | 74HC595D,112 | [DigiKey](https://www.digikey.com/en/products/detail/nexperia-usa-inc/74HC595D-112/763550) | [datasheet link](https://assets.nexperia.com/documents/data-sheet/74HC_HCT595.pdf) | U1 |
0.1 µF Ceramic Capacitor, +/-10%, X7R, 50V, 0805 package |10 | 0.2750 | $2.75 | KEMET | C0805F104K5RACTU | PRLTA 109 |n/a | C2, C4, C6, C7, C8, C9, C10, C11, C12, C16

**1. Power Regulation & Protection** 
| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----| 
2.1mm x 5.5mm PCB DC Barrel Jack | 1 | $1.25 | $1.25 | CUI Devices | PJ-102AH | [DigiKey](https://www.digikey.com/en/products/detail/cui-devices/PJ-102AH/408448) | [Datasheet](https://www.cuidevices.com/product/resource/pj-102ah.pdf) | J1 |
500mA Fast-Act Subminiature Fuse | 1 | $0.85 | $0.85 | Littelfuse | 0273.500V | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | F1 |
+5V 1.5A Linear Voltage Regulator | 1 | $1.53 | $1.53 | STMicroelectronics | L7805ABV-DG | [DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805ABV-DG/3945936) | [Datasheet](https://www.st.com) | U1 |
0.33 µF, 50V Ceramic Input Filter Cap | 1 | $0.25 | $0.25 | TDK Corporation | FG28C0G1H334JNT06 | [DigiKey](https://www.digikey.com) | [Datasheet](https://www.digikey.com) | C1 |
0.1 µF, 50V Ceramic Output Filter Cap | 1 | $0.15 | $0.15 | KEMET | K104K15X7RF53L2 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | C2 |
12V DC 700mA AC/DC Wall Adapter | 1 | $7.58 | $7.58 | Triad Magnetics | WSU120-0700 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | External (J1) 

**2. Microcontroller Core & Environmental Sensing** 
| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----| 
PIC18F57Q43 Curiosity Nano Board | 1 | $0.00 | $0.00 | Microchip | DM164150 | [Microchip](https://www.microchip.com) | [Datasheet](https://ww1.microchip.com) | U2 |
1x14 Female Pin Headers (0.1" Pitch) | 2 | $0.65 | $1.30 | Sullins Connector | PPPC141LFBN-RC | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | Socket for U2 |
MCU Target 0.1 µF, 50V Bypass Caps | 2 | $0.15 | $0.30 | KEMET | K104K15X7RF53L2 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | C3, C4 |
DHT20 Temp & Humidity Sensor (I²C) | 1 | $4.50 | $4.50 | Adafruit / Aosong | 5183 / DHT20 | [Adafruit]([suspicious link removed]) | [Datasheet](https://cdn-shop.adafruit.com/product-files/5183/5193\_DHT20.pdf) | U5 |
1x4 Female Socket Header (0.1" Pitch) | 1 | $0.25 | $0.25 | Sullins Connector | PPPC041LFBN-RC | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | Socket for U5 |
Sensor VDD 0.1 µF, 50V Bypass Cap | 1 | $0.15 | $0.15 | KEMET | K104K15X7RF53L2 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | C5 |
4.7 kΩ, 1/4W Axial Resistors (I²C Pull-Up) | 2 | $0.10 | $0.20 | Yageo | CFR-25JB-52-4K7 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | R5, R6

**3. Communication, Expansion & User Interface**
| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
8-Pin (2x4) Shrouded Ribbon Header | 1 | $1.10 | $1.10 | Molex | 0702460801 | [DigiKey](https://www.digikey.com/en/products/detail/molex/0702460801/760165) | [Datasheet](https://www.molex.com) | J2 | 
8-Conductor Flat Ribbon Cable Assembly | 1 | $2.10 | $2.10 | Molex | 0151660081 | [DigiKey](https://www.digikey.com) | [Datasheet](https://www.molex.com) | Cable for J2 |
1x6 Male Expansion Header (0.1") | 1 | $0.30 | $0.30 | Amphenol FCI | 68000-106HLF | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | J3 |
Red 3mm Through-Hole Debug LED | 1 | $0.20 | $0.20 | Lumex | SSL-LX3044GD | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | D1 |
300 Ω, 1/4W Resistor (LED Current Limit) | 1 | $0.10 | $0.10 | Yageo | CFR-25JB-52-300R | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | R4 |
6mm x 6mm Tactile Pushbuttons | 2 | $0.35 | $0.70 | C&K | PTS645SM43SMTR92 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | SW1, SW2 |
10 kΩ, 1/4W Pull-Up Resistors | 2 | $0.10 | $0.20 | Yageo | CFR-25JB-52-10K | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | R2, R3 |
0.1 µF, 50V Debounce Capacitors | 2 | $0.15 | $0.30 | KEMET | K104K15X7RF53L2 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | C6, C7

**4. Test Points, Debugging Hardware & Prototyping**
| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
PCB Miniature Test Point Loop Terminals | 6 | $0.28 | $1.68 | Keystone Electronics | 5000 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | TP1, TP2, TP3, TP4, TP5, TP6 |
2-Pin 0.1" Shorting Jumpers/Shunts | 2 | $0.12 | $0.24 | TE Connectivity | 382811-6 | [DigiKey](https://www.digikey.com) | [Datasheet]([suspicious link removed]) | Debug Shunts |

### Total Subsystem Hardware Cost: **$25.43**
