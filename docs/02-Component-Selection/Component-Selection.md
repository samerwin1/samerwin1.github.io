---
title: Component Selection
---
**Description**

This page shows the process of choosing the hardware for the distance-sensing subsystem of the Private-Use Door Automation project. The tables below show the options that were proposed, each with a list of pros and cons related to the constraints and desired results of the design.


**Emitter**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](OPB732(Reflective%20Switch).png)<br>Option 1.<br> OPB732 Long Distance Reflective Switch<br>$4.61/each<br>[link to product](https://www.digikey.com/en/products/detail/tt-electronics-optek-technology/OPB732/1637069)                 | \*Emmiter & Detector in one package<br>\* Affordable<br>\* Already familiar with<br>\* Housing to reduce ambient light sensitivity                                               | \* Low range<br>\* Low forward current<br>\* Lower wavelength<br>\* Most expensive |
| ![](TSAL6200(IR%20Emitter).png)<br>Option 2.<br>TSAL6200 IR Emitting Diode <br> $0.49/each <br> [Link to product](https://www.digikey.com/en/products/detail/vishay-semiconductor-opto-division/TSAL6200/1681339?s=N4IgTCBcDaIC4GcCGAbAbGADJkBdAvkA) | \* Least expensive <br>\* High radiant power/intensity<br>\* Higher peak wavelength<br>\* High forward current | \* No focused casing/lense<br>\* Lower peak forward current(although with higher duty cycle)\* Does not include detector                                                         |
| ![](1N6265(IR%20Emitter).png)<br>Option 2.<br>1N6265 IR LED Emitter<br> $0.95/each <br> [Link to product](https://www.jameco.com/z/1N6265-Fairchild-onsemi-LED-IR-Emitter-Infrared-TO-46-940nm-1us-Rise-100mW_2285031.html) | \* Inexpensive<br>\* More focused casing<br>\* High forward current<br>\* High power dissipation | \* Highest forward voltage<br>\* Low radiant power<br>\* Radiant intensity not listed<br>\* Does not include detector                                                       |

**Choice:** Option 2: TSAL6200 IR Emitting Diode

**Rationale:** While it is tempting to use the OPB732 since it is a paired package, our system needs a higher radiant intensity in order to detect objects further away. Additionally, the higher peak wavelength is ideal in order to distinguish the sensor from ambient visible light sources. While the peak forward currents ratings of the other two options are slightly higher, it is ideal that the TSAL6200 is rated for a higher pulse duty cycle at its peak which improves the refresh rate of the system. Lastly, it is very inexpensive.


**Detector**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](OPB732(Reflective%20Switch).png)<br>Option 1.<br> OPB732 Long Distance Reflective Switch<br>$4.61/each<br>[link to product](https://www.digikey.com/en/products/detail/tt-electronics-optek-technology/OPB732/1637069)                 | \*Emmiter & Detector in one package<br>\* Affordable<br>\* Already familiar with<br>\* Housing to reduce ambient light sensitivity                                               | \* Low power dissipation<br>\* Higher dark current<br>\* Lower breakdown voltage<br>\* Most expensive |
| ![](QSB34ZR(Photodiode).png)<br>Option 2.<br>QSB34ZR Silicon Pin Photodiode <br> $1.14/each <br> [Link to product](https://www.digikey.com/en/products/detail/onsemi/QSB34ZR/1053818?s=N4IgTCBcDaIIoGUBCBmALALQEogLoF8g) | \* Affordable <br>\* High radiant sensitivity<br>\* Daylight-blocking filter<br>\* Good power dissipation | \* Very wide reception angle<br>\* Surface mount package(harder to keep in place when not directly on PCB)<br>\* Does not include emitter                                                        |
| ![](BPV23NF(Photodiode).png)<br>Option 2.<br>BPV23NF Silicon PIN Photodiode<br> $1.08/each <br> [Link to product](https://www.digikey.com/en/products/detail/vishay-semiconductor-opto-division/BPV23NF/1681143) | \* Affordable<br>\* Daylight-blocking filter<br>\* High radiant sensitivity<br>\* High power dissipation<br>\* Low dark current | \* Side-mounted(could be hard to place at correct angle for emitter)<br>\* Wide range of detectable wavelength<br>\* Does not include emitter                                                        |

**Choice:** Option 3: BPV23NF Silicon PIN Photodiode

**Rationale:** As stated for the emitter selection, a two-in-one package would be convinient, but it is more important that the detector is low-noise yet sensitive enough for precise, longer-range use. Between the QSB34ZR and the BPV23NF, they have very similar features/specifications. The main distinction between them is the reception angle (much higher on the QSB34ZR) which is not ideal for focused reflective sensing. Additionally, the surface-mount packaging would make it more difficult to intsall in a wired configuration. In order to reduce the amount of environmental noise and uphold practical installation, the BPV23NF was chosen.


**Operational Amplifier**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](LMC6482(OpAmp).png)<br>Option 1.<br> LMC6482 <br>$5.62/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LMC6482IN-NOPB/364330)                 | \*Affordable<br>\* Low input bias current<br>\* Rail to rail<br>\* Low quiescent current                                              | \* Lower speed<br>\* Lowest slew rate<br>\* Headroom loss near rails<br>\* Sensitive to heavy loads |
| ![](MCP6022(OpAmp).png)<br>Option 2.<br> MCP6022 <br> $1.86/each <br> [Link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP6022-I-P/417828) | \* Least expensive option <br>\* High GBW<br>\* High slew rate<br>\* Rail to rail with minimal loss<br>\* Low noise<br>\* Low quiescent current | \* Limited load drive<br>\* Lowest operating supply range                                                         |
| ![](OPA2704(OpAmp).png)<br>Option 2.<br> OPA2704 <br> $6.36/each <br> [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/OPA2704UA-2K5/1572356) | \* Balance of performance and power<br>\* Rail to rail<br>\* Lowest input offset<br>\* Acceptable quiescent current | \* Most expensive option<br>\* Lower speed<br>\* Lower slew rate<br>\* No through-hole packages in stock                                                         |

**Choice:** Option 2: MCP6022

**Rationale:** The MCP6022 seems most capable for handling quick-changing analog signals, has low noise, and should have minimal voltage loss when near the rails of the supply. All of these features make it ideal for amplifying the signal of the photodiode without corrupting important data.



**MOSFET**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](2N7000(MOSFET).png)<br>Option 1.<br> 2N7000 <br>$0.21/each<br>[link to product](https://www.digikey.com/en/products/detail/diotec-semiconductor/2N7000/13164314)                 | \*Least expensive<br>\* Current rating meets goal<br>\* Easy to source                                             | \* Lower current rating than other options<br>\* Higher Rds(on)<br>\* Lower power dissipation |
| ![](IRLZ44NPBF(MOSFET).png)<br>Option 2.<br> IRLZ44NPBF <br> $1.53/each <br> [Link to product](https://www.digikey.com/en/products/detail/infineon-technologies/IRLZ44NPBF/811808) | \* Affordable <br>\* Very high current rating<br>\* High power dissipation | \* More expensive than other options<br>\* High Input Capacitance                                                         |
| ![](FQP13N06L(MOSFET).png)<br>Option 2.<br> FQP13N06L <br> $0.68/each <br> [Link to product](https://www.digikey.com/en/products/detail/rochester-electronics-llc/FQP13N06L/13455336) | \* Inexpensive<br>\* Most balanced performance vs cost<br>\* Mid-grade current rating | \* Only sold in bulk<br>\* High shipping fee<br>\* Higher input capacitance                                                       |

**Choice:** Option 2: IRLZ44NPBF

**Rationale:** Since the MOSFET will be used for running high current through the IR Emitters, the high current rating and power dissipation make it ideal. Although it has a higher input capacitance, the lower frequency of the pulse signal does not cause concern in this area. While it is the most expensive option, it is still affordable and nowhere near budget-breaking.


**Voltage Regulator**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](LM7805(Regulator).png)<br>Option 1.<br> LM7805 Linear Voltage Regulator<br>$0.33/each<br>[link to product](https://www.digikey.com/en/products/detail/taejin/lm7805t/22237260)                 | \*Affordable<br>\* Fits project goals<br>\* Already provided                                             | \* Higher voltage dropout<br>\* Lower max current<br>\* Not optimized for efficiency |
| ![](LM1085IT-5.0(Regulator).png)<br>Option 2.<br> LM1085IT-5.0 Linear Voltage Regulator <br> $2.13/each <br> [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/LM1085IT-5-0-NOPB/363564) | \* Higher current capability <br>\* Low voltage dropout<br>\* Better regulation characteristics | \* Expensive<br>\* Poor efficiency                                                         |
| ![](LM2941T(Regulator).png)<br>Option 2.<br> LM2941T Linear Voltage Regulator <br> $1.72/each <br> [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/LM2941T-NOPB/148144) | \* Lowest voltage dropout<br>\* Low noise<br>\* Ranging output voltage| \* Expensive<br>\* Lowest current rating                                                      |

**Choice:** Option 1: LM7805 Linear Voltage Regulator

**Rationale:** The LM7805 meets the subsystem's needs for supply current, input voltage, and output voltage. On top of meeting the requirements, it has already been provided and therefore there is no reason to order and implement a different option.