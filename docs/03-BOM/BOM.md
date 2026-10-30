
## Overview
This Bill of Materials accounts for all physical components shown on the Subsystem Schematic DHT20 Schematic, including test points, status LEDs, socket headers, and debugging hardware.

## Bill of Materials for Temperature/Humidity Sensing Subsystem 

**1. Power Regulation & Protection** 

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----| 
2.0mm x 5.5mm PCB DC Barrel Jack | 1 | $0.75 | $0.75 | Same Sky (Formerly CUI Devices) | PJ-102A | [DigiKey](https://www.digikey.com/short/0d13jcq8) | [Datasheet Link](https://www.sameskydevices.com/product/resource/pj-102a.pdf) | J1 |
500mA Fast-Act Fuse | 1 | $1.60 | $1.60 | Littelfuse Inc. | 0251.500MRT1L | [DigiKey](https://www.digikey.com/short/02qd2ppr) | [Datasheet](https://www.littelfuse.com/assetdocs/littelfuse-fuse-251-253-datasheet?assetguid=f47a0bb7-8ede-4679-9646-7114c3787688) | F1 |
+5V 1.5A Linear Voltage Regulator | 1 | $1.53 | $1.53 | STMicroelectronics | L7805ABV-DG | [DigiKey](https://www.digikey.com/short/7b7r0r3r) | [Datasheet Link](https://www.st.com/content/ccc/resource/technical/document/datasheet/41/4f/b3/b0/12/d4/47/88/CD00000444.pdf/files/CD00000444.pdf/jcr:content/translations/en.CD00000444.pdf) | U1 |
0.33 µF, 50V Ceramic Input Filter Capacitor | 1 | $0.58 | $0.58 | Murata Electronics | RCER71H334K1A2H03B | PRLTA 109 | [Datasheet Link](https://pim.murata.com/asset/pim4/ceramicCapacitorLead/RCE_X7R_X7S_25V-100V_E_PDF_CERAMICCAPACITORLEAD?lastModifiedDatetime=20250909130221) | C1 |
0.1 µF, 50V Ceramic Output Filter Capacitor | 1 | $0.15 | $0.15 | KEMET | C315C104K1R5TA | PRLTA 109 | [Datasheet Link](https://yageogroup.com/content/datasheet/asset/file/KEM_C1050_GOLDMAX_X7R) | C2 |
12V DC 700mA AC/DC Wall Adapter | 1 | $7.58 | $7.58 | Triad Magnetics | WSU120-0700 | [DigiKey](https://www.digikey.com/short/7wptwdfp) | [Datasheet Link](https://catalog.triadmagnetics.com/Asset/WSU120-0700.pdf) | External (J1) 

**2. Microcontroller Core & Environmental Sensing** 

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----| 
PIC18F57Q43 Curiosity Nano Board | 1 | $0.00 | $0.00 | Microchip | DM164150 | [Microchip](https://www.microchip.com) | [Datasheet Link](https://ww1.microchip.com) | U2 |
1x14 Female Pin Headers (0.079" Pitch) | 2 | $0.92 | $1.84 | Adam Tech | 2RS1-12-G | [DigiKey](https://www.digikey.com/short/qn5b9c4r) | [Datasheet Link](https://app.adam-tech.com/products/download/data_sheet/202413/2rs1-xx-g-data-sheet.pdf) | Socket for U2 |
MCU Target 0.1 µF, 50V Bypass Capacitor | 2 | $0.15 | $0.30 | KEMET | C315C104K1R5TA | PRLTA 109 | [Datasheet Link](https://yageogroup.com/content/datasheet/asset/file/KEM_C1050_GOLDMAX_X7R) | C3, C4 |
DHT20 Temp & Humidity Sensor (I²C) | 1 | $4.50 | $4.50 | Adafruit / Aosong | 5183 / DHT20 | [Adafruit Industries LLC](https://www.digikey.com/short/hbqt7t73) | [Datasheet Link](https://cdn-shop.adafruit.com/product-files/5183/5193_DHT20.pdf) | U5 |
1x4 Female Socket Header (0.079" Pitch) | 1 | $0.92 | $0.92 | Adam Tech | 2RS1-12-G | [DigiKey](https://www.digikey.com/short/qn5b9c4r) | [Datasheet Link](https://app.adam-tech.com/products/download/data_sheet/202413/2rs1-xx-g-data-sheet.pdf) | Socket for U5 |
Sensor VDD 0.1 µF, 50V Bypass Capacitor | 1 | $0.15 | $0.15 | KEMET | C315C104K1R5TA | PRLTA 109 | [Datasheet Link](https://yageogroup.com/content/datasheet/asset/file/KEM_C1050_GOLDMAX_X7R) | C5 |
4.7 kΩ, 1/4W Axial Resistors (I²C Pull-Up) | 2 | $0.10 | $0.20 | Stackpole Electronics Inc | CF14JT4K70 | PRLTA 109 | [Datasheet Link](https://www.seielect.com/catalog/SEI-CF_CFM.pdf) | R5, R6

**3. Communication, Expansion & User Interface**

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
8-Pin (2x4) Shrouded Ribbon Header | 1 | $0.95 | $0.95 | Adafruit Industries LLC | 4939 | [DigiKey](https://www.digikey.com/short/r3wnw082) | n/a | J2 | 
8-Conductor Flat Ribbon Cable Assembly | 1 | $2.10 | $2.10 | Molex | 0151660081 | [DigiKey](https://www.digikey.com) | [Datasheet Link](https://www.molex.com) | Cable for J2 |
1x6 Male Expansion Header (0.079") | 1 | $0.29 | $0.29 | Adam Tech | 2PH1-11-UA | [DigiKey](https://www.digikey.com/short/brm0z7ff) | [Datasheet Link](https://app.adam-tech.com/products/download/data_sheet/200457/2ph1-xx-ua-data-sheet.pdf) | J3 |
Red 9mm Through-Hole Debug LED | 1 | $0.66 | $0.66 | Kingbright | WP7113SURDK14V | PRLTA 109 | [Datasheet Link](https://www.kingbrightusa.com/images/catalog/SPEC/WP7113SURDK14V.pdf) | D1 |
300 Ω, 1/4W Resistor (LED Current Limit) | 1 | $0.10 | $0.10 | KOA Speer Electronics, Inc. | CF1/2CT52R301J | PRLTA 109 | [Datasheet Link](https://mm.digikey.com/Volume0/opasdata/d220001/medias/docus/6165/2019_CF_Series.pdf) | R4 |
6mm x 6mm Tactile Pushbuttons | 2 | $0.35 | $0.70 | SCHURTER Inc. | 1301.9302 | PRLTA 109 | [Datasheet Link](https://www.schurter.com/en/datasheet/typ_6x6_mm_tact_switches.pdf) | SW1, SW2 |
10 kΩ, 1/4W Pull-Up Resistors | 2 | $0.10 | $0.20 | Stackpole Electronics Inc | CF14JT10K0 | PRLTA 109 | [Datasheet Link](https://www.seielect.com/catalog/SEI-CF_CFM.pdf) | R2, R3 |
0.1 µF, 50V Debounce Capacitors | 2 | $0.15 | $0.30 | KEMET | C315C104K1R5TA | PRLTA 109 | [Datasheet Link](https://yageogroup.com/content/datasheet/asset/file/KEM_C1050_GOLDMAX_X7R) | C6, C7

**4. Test Points, Debugging Hardware & Prototyping**

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacture** | **Manufacturer #** | **Vendor Link** |**Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
PCB Miniature Test Point Loop Terminals | 6 | $0.27 | $1.62 | Keystone Electronics | 5001 | [DigiKey](https://www.digikey.com/short/9c7jq7r7) | [Datasheet Link](https://www.keyelco.com/userAssets/file/K75p62.pdf) | TP1, TP2, TP3, TP4, TP5, TP6 |
2-Pin 0.177" Jumpers | 2 | $0.15 | $0.30 | Adam Tech | MSC-G | [DigiKey](https://www.digikey.com/short/b591f53h) | [Datasheet Link](https://app.adam-tech.com/products/download/data_sheet/203327/msc-g-data-sheet.pdf) | Debug Shunts |
28-Pin 0.100" Header for Microcontroller | 2 | $0.50 | $1.00 | Same Sky (Formerly CUI Devices) | SSK02-FPH-254-A28 | [DigiKey](https://www.digikey.com/short/tnm288fh) | [Datasheet Link](https://www.sameskydevices.com/product/resource/ssk02-fph-254.pdf) | Microcontroller Mount |
4-Pin 0.100" Header for DHT20 | 1 | $0.42 | $0.42 | Würth Elektronik | 61300411821 | [DigiKey](https://www.digikey.com/short/nmb70r0f) | [Datasheet Link](https://www.we-online.com/components/products/datasheet/61300411821.pdf) | Temperature & Humidity Sensor Mount

### Total Subsystem Hardware Cost: **$25.69** for All Cost & **18.91** While using Peralta 109 Resources
