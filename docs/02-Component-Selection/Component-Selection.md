---
title: Component Selection for Design 
---

**Tempature & Humidity Sensing Transmission**

| **Component 1: Temperature & Humidity Sensor **                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](SNS-DH11.jpg)<br>Option 1.<br> 1188-SNS-DHT11-ND<br>$3.95/each<br>[link to product](https://www.digikey.com/short/f338bv47)                 | \* high humidity range<br>\* Only needs one GPIO pin <br>\* Compact for small project deisgn                                               | \* Lower accuracy<br>\* Maximum sampling rate 1HZ |
| ![](26085_DHT.jpg)<br>\* Option 2. <br>\* CANADUINO 26085 <br>\* $2.39/each <br>\* [Link to product](https://www.digikey.com/short/wm7pmcbw) | \* Cheaper than other options <br>\* Wide voltage range <br> \* 16 bit output provides high resolution data | * Low relative humidity(RH) limit <br>\* lower quality DHT11                                                         |
| ![](DHT22.jpg)<br>\* Option 3. <br>\*  1188-SNS-DHT22-ND <br>\* $7.30/each <br>\* [Link to product](https://www.digikey.com/short/mtzfnvnt) | \*High precision <br>\* Fast response time <br> \* Industry Stadard | * Expensive <br>\* Harder to hand solder  <br>\* Require external pull-up resistors                                                        |

**Choice:** Option 1: 1188-SNS-DHT11-ND Sensor 

**Rationale:** Since our design does not require precise readings and operates natively on a 5V rail, the DHT11 is the best choice. Not only is the component within budget constraints, it also only uses one GPIO pin leaving the remaining pins open for UART communication. 


| **Component 2: 5v Linear Voltage Regulator **                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](L7805ABV-DG.jpg)<br>Option 1.<br> L7805ABV-DG<br>$1.53/each<br>[link to product](https://www.digikey.com/short/15pzw22v)                 | \* High output accuracy<br>\* Wide operating temperature <br>\* Stable over a wide input voltage range                                               | \* Gets hot too quickly <br>\* Requires a minimum of 2v dropout voltage |
| ![](MC7805CTG.jpg)<br>\* Option 2. <br>\* MC7805CTGOS-ND<br>$1.01/each <br>\* [Link to product](https://www.digikey.com/short/tq2pv7h9) | \* Low dropout voltage <br>\* Built in heatsink <br> \* High current capability | * Poor power efficiency <br>\* Maximum output current limited to 250 mA  <br>\* Consumes a operating current of 5mA to 6.5mA                                                     |
| ![](MCP1700.jpg)<br>\* Option 3. <br>\*  MCP1700-5002E/TO-ND <br>\* $0.50/each <br>\* [Link to product](https://www.digikey.com/short/9zw8dnb0) | \*Extremely inexpensive  <br>\* Very low operating current(µA) <br> \* Built in circuit protection | * Narrow input voltage margin <br>\* Requires input/output filter capacitros for sabaility                                            |

**Choice:** Option 1: L7805ABV-DG

**Rationale:** The L7805ABV-DG was selected due to its capability of sourcing a 1.5A max output current which will provide a safe current for our design and its built in circuit protection incase of a short circuit. It is also a standard stock component, even being used in some of the in class Lab, also providing thermal protection feature such as a heatsink to reduce heat with high voltage.


| **Component 3: External Power Supply **                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](PSAC05R2.jpg)<br>Option 1.<br>993-PSAC05R-050L6-R-ND<br>$5.56/each<br>[link to product](https://www.digikey.com/short/p8mf59r8)                 | \* high efficiency <br>\* Reliable output <br>\* Interchangeable AC plugs                                                | \* AC plugs sold separately<br>\* Limited to 5 watts |
| ![](16-00078.jpg)<br>\* Option 2. <br>\* 839-16-00078-ND <br>\* $7.51/each <br>\* [Link to product](https://www.digikey.com/short/t1zb5h8q) | \* Wide input range <br>\* Standard output connector <br> \* High energy efficiecy | * Low power output <br>\* Low operating tempature                                                         |
| ![](WSU120-0700.jpg)<br>\* Option 3. <br>\*  WSU120-0700 <br>\* $7.58/each <br>\* [Link to product](https://www.digikey.com/short/mtzfnvnt) | \*Clean and regulated output <br>\* Long cord length <br> \* Affordable | * Narrow operating temperature                                            |

**Choice:** Option 3: WSU120-0700 AC/DC WALL MNT ADAPTER 12V 8.4W

**Rationale:** The WSU120-0700 was chosen since it satisfies the regulator dropout requirements, for example our chosen voltage regulator requires a minimum of 7 volts which our 12V DC output satisfies. The 700 mA at 12v DC provides significant current headroom to pass the 25 percent current safety margin, it also has a integrated barrel plug that is compatible with the barrel jack on our PCB. 

