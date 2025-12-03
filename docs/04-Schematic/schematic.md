---
title: Schematic
---

## Overview

This page shows the electrical schematic of the IR Distance-Sensing Subsystem. The different sections of the schematic show different "modules" of the whole subsystem. As labeled, the modules include the Power Supply/Voltage Regulator providing power to all components, the 8-pin ribbon wire connecter for connection between subsystems, the IR emitters, the filtered and amplified photodiodes, and the microcontroller handling logic and communication.

## Schematic PNG

![schematic](IndividualSubsystemSchematicV2.png){style width:"350" height:"300;"}



## Resouces

The schematic as a PDF download is available [*here*](EGR304-IndividualSubystemDesignV2.pdf), and the Zip folder of the project [*here*](EGR304-IndividualSubystemDesign.zip).

## Explanation

### **Power Supply/Voltage Regulator**

This module of the schematic shows how power is being supplied to the subsystem. At the start of the circuit, 12V DC is supplied through a barrel jack connector. This 12V is sent through a 1.25A fuse for current overdraw protection, then into a linear voltage regulator which supplies the rest of the subsystem with a steady 5V DC supply.

### **Microcontroller**

This module shows the PIC18F57Q43-CNANO, the brain/logic processor of the subsystem. Several net labels show pins on the PIC that are connected to points in different modules. These connections include PWM outputs to the IR Emitters module, ADC inputs from the IR Photodiodes module, and inputs/outputs to/from the Ribbon Cable Connector module. Also connected to the PIC are a pushbutton and an LED for debugging purposes, as well as an extra digital and an extra analog connection to support any required additions to the design.

### **IR Emitters**

This module shows the IR emitters being driven by N-channel MOSFETs in order to send out a powerful pulse signal of IR light. This light hits the objects on either side of the door and reflects back into the photodiodes with an intensity that is proportional to distance. The Emitter 1 and Emitter 2 tags show the 20kHz pulsed input from the microcontroller going into their respective MOSFET gates. Each time a pulse is received the MOSFET opens the flow from 5V to GND, sending a high current through the IR Emitter, then closes it again. This setup allows the IR Emitters to flash brightly at 20kHZ, allowing it to be distinguished from background IR in the environment. The high current allows the emitters to still output a strong enough radiance for the photodiodes to pick up on.

### **IR Photodiodes**

This module contains the IR photodiodes and supporting circuitry. At the left side are two voltage dividers which provide reference voltages (~0.1V and 2.5V) for the operational amplifiers. Immediately to the right of these are the supply nodes of the operational amplifier (5V for VDD and GND for VSS). To the right of the supply nodes is the dual-stage amplification of the photodiode. The first stage is a transimpedance amplifier which converts the tiny current of the photodiode into a measurable voltage from ~0.1-4.9V. The 22pF capacitor is in parallel with the feedback resistor to filter out the high frequency AC noise while still picking up on the 20kHz signal of the emitters. The second stage is an inverting amplifier with a gain of 1. This flips the extremes of the voltage so that 0.1V becomes 4.9V and vice versa. This means that a small current from the photodiode (an object being far away and therefore reflecting low amounts of light) translates to a large voltage. A larger current from the photodiode (an object being near) translates into a small voltage. The analog output is then sent to the microcontoller which translates the voltages into distance values.

The right side of this module is the second photodiode circuit, and works exactly the same way.

### **Ribbon Cable Connector**

The final module shows the connections coming in from/going out to the other subsystems. This allows the subsystem to receive analog input about rotational position from the Rotary Encoder Subsystem and inform the the Motor Subsystem to start, stop, or continue rotaion.

### **Result**

The combination of these modules results in the subsystem performing its required function: sensing how far away the nearest object is, checking it against the rotational postition provided by the rotary encoder, and communicating to the motor accordingly.