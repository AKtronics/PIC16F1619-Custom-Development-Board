# PIC16F1619-Custom-Development-Board

A professional-quality development board built from scratch using the PIC16F1619 microcontroller. Designed and simulated as my 2nd pcb project. This is a small compact version exclusively for PIC16F16!9 microcontroller usable for circuit development, testing educational purpose.
---

## Project Overview

This is a custom-built development board designed for the **PIC16F1619** 8-bit microcontroller. The board supports ICSP programming, UART communication via an external USB-to-Serial module, and breadboard friendly pinout access.

---

## Table of Contents

- [Features](#features)  
- [Schematic and PCB](#schematic-and-pcb)  
- [Pin Mapping](#pin-mapping)  
- [Getting Started](#getting-started)  
- [Tools Used](#tools-used)  
- [Learning Outcomes](#learning-outcomes)  
- [Future Improvements](#future-improvements)  

---

## Features

- Based on **PIC16F1619** (20-pin DIP package)  
- **Low Voltage Programming (LVP)** via ICSP header  
- Onboard **reset circuitry**  
- External **UART debug interface** (TX/RX header for CH340/FT232)  
- **Power LED** + optional user LED  
- All **GPIOs broken out** to headers  
- Stable **5V operation** using external regulated supply or USB power  

---

## Schematic and PCB

- Designed using **KiCad / EasyEDA**  
- Includes decoupling capacitors, pull‑up resistor for MCLR, and test points  
- Supports clean routing with minimal vias  
- **2-layer PCB**, 5×5 cm, single-sided component layout  

_schematics_

![image](https://github.com/user-attachments/assets/eaebf8b0-f1c7-4c44-a0ba-eeea0f0589d4)

_PCB_


![image](https://github.com/user-attachments/assets/dab0b91f-e6cc-4865-b349-4f23e1768441)

---

## Pin Mapping

| Function         | PIC Pin | Board Label |
|------------------|---------|-------------|
| VDD              | 1       | VCC         |
| GND              | 20      | GND         |
| MCLR (Reset)     | 4       | RST         |
| ICSPDAT          | 19      | PGD         |
| ICSPCLK          | 18      | PGC         |
| UART TX          | 6  (RC4)| TX          |
| UART RX          | 5  (RC5)| RX          |

---

## Getting Started

### Requirements

- MPLAB X IDE  
- XC8 Compiler  
- PICkit 3 or 4 for programming  
- CH340 or FT232 USB-to-Serial adapter for UART debugging  

### Programming Steps

1. Connect PICkit to ICSP header (PGC/PGD/VPP/VDD/GND).  
2. Enable LVP in the config bits.  
3. Flash using MPLAB X.  
4. Connect CH340 (TX → RX, RX → TX, GND → GND) for UART monitoring.
5. Remap UART TX/RX to RC4 and RC5 using PPS

---

## Tools Used

- **MPLAB X IDE** + XC8 Compiler  
- **LTSpice / Multisim** for simulation  
- **VS Code** for firmware editing  
- **KiCAD** for schematic and PCB  

---

## Learning Outcomes

- Improved upon reading Microchip datasheets  
- Understood pin configuration, memory layout, config bits  
- Learned how to design PCBs with proper decoupling, voltage regulation, ESD protection, signal noise preduction, reverse polarity protection, ICSP routing  
- Learned integrating usb interface
- Understood practical PCB design constraints, like trace width, via size, component clearance, and EMI mitigation
- Improvised and gained experience in thermal management, data lines coupling, ground and power plane pour
---

## Future Improvements

- Integrate USB‑C for power  
- Support ICD debugging via header  
- SMT version (v1.1 planned)  
- Copper pour + ground plane for better EMI
- Add ICD (In-Circuit Debug) Header

---

