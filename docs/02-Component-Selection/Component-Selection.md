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


| **Component 3: External Power Supply **      






1. XC1259TR-ND surface mount crystal

    ![](image1.png)

    * $1/each
    * [link to product](http://www.digikey.com/product-detail/en/ECS-40.3-S-5PX-TR/XC1259TR-ND/827366)

    | Pros                                      | Cons                                                             |
    | ----------------------------------------- | ---------------------------------------------------------------- |
    | Inexpensive                               | Requires external components and support circuitry for interface |
    | Compatible with PSoC                      | Needs special PCB layout.                                        |
    | Meets surface mount constraint of project |

1. CTX936TR-ND surface mount oscillator

    ![](image3.png)

    * $1/each
    * [Link to product](http://www.digikey.com/product-detail/en/636L3I001M84320/CTX936TR-ND/2292940)

    | Pros                                                              | Cons                |
    | ----------------------------------------------------------------- | ------------------- |
    | Outputs a square wave                                             | More expensive      |
    | Stable over operating temperature                                 | Slow shipping speed |
    | Direct interface with PSoC (no external circuitry required) range |

**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.
