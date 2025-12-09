---
title: Power Budget
---

## Description

This page shows the power budget for the major components involved in the circuitry of the Distance Sensing Subsystem. The power budget was created to theorize maximum possible current draw from each major electrical component, as well as describe how the power for the system will be supplied. This ensures that the power source/voltage regulator are capable of providing all necessary current to the subsystem without being overloaded.

## Power Budget

![Power Budget](EGR%20304%20Team%20103%20Individual%20Power%20Budget.png)
***Note:*** *The PIN Photodiode has been purposefully omitted from the power budget as it does not draw any current from the power supply when functioning as intended. Intended functionality causes it to produce current by absorbing photons. Furthermore, any current that could be drawn by it would be insignificant (on the order of nanoamps to microamps).*

## Conclusions

From the Power Budget, it is clear that the 12V wall supply and 5V linear regulator will be sufficient to safely power the subsytem with extra headroom for minor components (resistors, capacitors, etc). It also helps in deciding what size fuse to use at the power supply of the subsystem. Since the maximum current draw of all components in the subsystem is just over 1 Amp, it makes sense to use the next size up in fuse options: 1.25 Amps.

## Resouces

The power budget as a PDF download is available [*here*](EGR%20304%20Team%20103%20Individual%20Power%20Budget.pdf), and a Microsoft Excel Sheet [*here*](EGR%20304%20Team%20103%20Individual%20Power%20Budget.xlsx).