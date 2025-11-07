---
title: Welcome
tags:
- tag1
- tag2
---
<center>
<font size= "6"> Seth Merwin Individual Datasheet</font><br>
as part of<br>
<font size= "8"> Private-Use Door Automation</font><br>
for<br>
<font size= "5"> Team 103 </font><br>

**Submission: month, DD, 2025**
</center>

## Introduction

This datasheet shows the details of my contribution to the project "Private-Use Door Automation". The different pages of the datasheet show resources such as the design process, materials, and cost of my own personally developed subsystem. This subsystem is one part of the greater whole system designed by Team 103.


### Project Summary

The goal of "Private-Use Door Automation" is to provide ease of access to consumers through the design of a self-calibrating, automaticly opening and closing door system. While automatic doors are nothing new, the vision is to bring the idea into private homes/properties while also making the technology inexpensive and easy to integrate. More specifically our target consumers are those with disabilities and their caregivers, however we want the product to appeal to anyone desiring efficiency and automation in their home.

The product will be installable on any lighter-weight swinging interior door. After a simple install, a single button press will open and promptly close the door while multiple sensors collect data along the path. From then on, the door will automatically open any time someone approaches from either side, wait a period of time, and then automatically close. The multiple sensors will be able to detect any obstacles in the way or variations from the typical path and stop the door from becoming hazardous.

The function of the product is acheived through the combination of four embedded subsystems:

* Infrared Distance-Sensing Subsystem (focus of this datasheet)
* Motor Subsystem
* Rotary Encoder Subsystem
* Resistive Flex Sensor Subsystem

These four subsystems each play a vital role and communicate with each other in order to control the final product. Each subsystem was designed by an individual member of the team. To learn more about the other subsystems, how they all work together, and the design process of the whole project, you can visit the [Team Report Website.](https://egr304-2025-f-103.github.io/)


### My Contribution

My personal contribution to the Private-Use Door Automation project is the Infrared Distance-Sensing Subsystem. It uses two IR emitter/detector pairs which are signal conditioned, amplified, and processed through a microcontroller to provide accurate distance measurements. One pair is placed on either side of the door in order to provide a view of its direct path.

During calibration the door opens 90 degrees and then closes. While this happens, the sensors store distance values of the nearest object in their view at several points along the path. In "standby mode", the sensors tell the motor to open the door once they detect a person approaching. As the door opens, they periodically check their current values with those stored during calibration. Any inequality in these values sends an alert through the system which stops the motor until the obstruction is clear.

This website was created to provide an understanding of how the subsystem was designed and brought to reality.

* To learn about the hardware components and their connections to the microcontroller, visit the ["Block Diagram" page.](https://samerwin1.github.io/01-Block-Diagram/Block-Diagram/)
* To understand why specific components were chosen, visit the ["Component Selection" page.](https://samerwin1.github.io/02-Component-Selection/Component-Selection/)
* To see the list of materials for the subsystem, visit the ["BOM" page.](https://samerwin1.github.io/03-BOM/BOM/)
* To visualize the electrical flow of the circuitry, visit the ["Schematic" page.](https://samerwin1.github.io/04-Schematic/schematic/)
* To see a breakdown of each component's current draw and how power is provided to the system, visit the ["Power Budget" page.](https://samerwin1.github.io/05-Power-Budget/Power-Budget/)
* To see the design of the PCB(Printed Circuit Board), visit the ["PCB Design" page.](https://samerwin1.github.io/06-PCB-Design/PCB-Design/)
* Finally, to see additional supporting information not included in the main pages, visit the ["Apendix" page.](https://samerwin1.github.io/Appendix/)
