---
title: Appendix - Main Page
---

## **Changes to Subsystem Hardware**

This appendix shows the block diagram and schematic used for testing the subsystem in place of the selected components which did not arrive in time. The changes are explained below:

### **Emitter/Detector**

Instead of the chosen emitter and detector, the [OPB732 Reflective Switch](https://www.digikey.com/en/products/detail/tt-electronics-optek-technology/OPB732/1637069) (shown in the Component Selection page) was used.

### **Operational Amplifier**

Instead of the chosen operational amplifier, the [MCP6004](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060) was used.

### **MOSFETs/PWM**

Since the MOSFETs were not obtained and there was so little time, I decided to remove the Pulse Width Modulation functionality from the emmiters and have them constantly on instead. This meant that they could not be powered by as strong of a current and therefore the range of distance sensing was reduced.

### **Resistor Values**

Finally, many resistor values had to be adjusted inside the amplification stage to provide proper voltage/current to the substituted components.

## **Conclusion**

While it was quite upsetting to be setback and unable to create the subsystem the way I wanted it, it was a success to be able to change things at the last minute and still show that my programming worked. In the end, I had a distance-sensing subsystem that could provide the basic functionality that was required. Additionally, it was able to connect to my teammates subsystems to function as a whole. This leads me to believe that if I was able to finish my project using the components I selected, it would be even more succesful with even greater range.