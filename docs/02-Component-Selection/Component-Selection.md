---
title: Component Selection Example
---

## Examples

### Style 1

**Tempature & Humidity Sensing Transmission**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](SNS-DH11.jpg)<br>Option 1.<br> 1188-SNS-DHT11-ND<br>$3.95/each<br>[link to product](https://www.digikey.com/short/f338bv47)                 | \* high humidity range<br>\* Only needs one GPIO pin <br>\* Compact for small project deisgn                                               | \* Lower accuracy<br>\* Maximum sampling rate 1HZ |
| ![](26085_DHT.jpg)<br>\* Option 2. <br>\* CANADUINO 26085 <br>\* $2.39/each <br>\* [Link to product](https://www.digikey.com/short/wm7pmcbw) | \* Cheaper than other options <br>\* Wide voltage range <br> \* 16 bit output provides high resolution data | * Low relative humidity(RH) limit <br>\* lower quality DHT11                                                         |
| ![](DHT22.jpg)<br>\* Option 3. <br>\*  1188-SNS-DHT22-ND <br>\* $7.30/each <br>\* [Link to product](https://www.digikey.com/short/mtzfnvnt) | \*High precision <br>\* Fast response time <br> \* Industry Stadard | * Expensive <br>\* Harder to hand solder  <br>\* Require external pull-up resistors                                                        |



**Choice:** Option 2: CTX936TR-ND surface mount oscillator

**Rationale:** A clock oscillator is easier to work with because it requires no external circuitry in order to interface with the PSoC. This is particularly important because we are not sure of the electrical characteristics of the PCB, which could affect the oscillation of a crystal. While the shipping speed is slow, according to the website if we order this week it will arrive within 3 weeks.

### Style 2

> Also acceptable, more markdown friendly

**External Clock Module**

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
