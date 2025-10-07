---
title: Individal Block Diagram
tags:
- tag1
- tag2
---

## Overview
This page shows a consructed block diagram representing the components of my personal subsystem which will be embedded into the greater project system. This subsystem focuses on sensing distances to objects from the door which the device will be installed on. There will be one sensor on either side of the door. Each time the device is triggered to open the door, the sensors will be verifying that nothing is in the path of the door as it is opening.

Every component in this subsystem will be powered by a 5 volt, 1.5 Amp voltage regulating circuit which itself will be supplied by a 9 volt power source. This is shown by the dashed-line box surrounding the components. The logic and communication functions will be handled by the Microchip PIC18F57Q43 Curiosity-Nano, symbolized by the large block in the center of the diagram. Each other block inside the 5 volt supplied box symbolizes a component which will be connected to the PIC18F57Q43. The directional arrows show whether the components are inputs or outputs and are labeled with their signal type, voltage level, and number of pins. The blocks inside the PIC18F57Q43 block show which pin the components are connected to and what peripheral of the device they will be using.

Finally, the block at the bottom of the diagram labeled "connector 3" symbolizes a header for the 8-wire ribbon cable which will be used to connect this subsytem to another subsystem (the motor system) within the project. As shown, my subsystem will be receiving 3 signal inputs (2 digital and 1 analog) and sending 2 outputs (both digital). This will allow the two subsystems to communicate with one another based on the programming of the PIC18F57Q43 devices. The goal is to have this distance-sensing subsytem tell the motor subsystem to start, continue running, or stop based on the data it is processing.


## Distance-Sensing Subsystem Block Diagram 


![Distance-Sensing Subsystem](images/Distance Sensors Subsystem Block Diagram.drawio.png)

