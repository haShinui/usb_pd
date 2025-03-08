# BrodBoost-PD
This USB Power Delivery adapter allows to request 20V, 15V, 12V, 9V, or 5V from a compatible power supply, eliminating the need for bulky converters or multiple adapters. A DIP switch selects the desired voltage. The adapter features a power LED, a fault LED, and a screw terminal block for easy wiring. Compatible with standard 2.54 mm breadboards, it provides a simple, compact power solution for prototyping and development.

I documented the process and the design, if you wish to learn more or see earlier versions, I made a short YouTube Video bellow

https://www.youtube.com/watch?v=EAl_JSd1YsA

BrodBoost-PD is an open-source project of Axiometa. Device is available for purchase on the [official website](https://axiometa.ai/product/brodboost-pd/)

![PD](https://github.com/user-attachments/assets/356bb271-0374-443e-8028-7578ce3baa5e)

# Overview

![pdp_top-1](https://github.com/user-attachments/assets/b0c6e7ff-caee-4a20-943f-16d27a50bbca)


# Device Configurations
BrodBoost-PD can be acquired and/or assembled in essentially three majors ways.

1. No breadboard rails, No Screw Terminal - Great for compact and intergrated solutions.
2. No Breadboard rail, Screw Terminal - Great for all solutions, requires no soldering.
3. Breadboard rails, Screw Terminal - Amazinf for breadboards, allows prototyping and attaching some loads on terminal

![IMG_4338](https://github.com/user-attachments/assets/fe125ee3-6045-4208-a7ba-f22d8e1c8ed7)


# Breadboard Compatibility
In the case of attached headers,the device becomes compatible with almost all BB400 & BB800 Solderless Breadboards

![compatibility_pdp1](https://github.com/user-attachments/assets/a417a1fb-0124-4bd5-ae57-e07c31d4e7c0)

# Voltage Selection
All voltage rails are connected, that includes both breadboard rails, screw terminal and solder pads. The voltages can be selected through the dip switches in a fashion shown bellow.

![dip_tutorial2](https://github.com/user-attachments/assets/cf4f1a10-5738-44a1-a36c-b9121f5f5b6c)

# Schematic
A USB-C receptacle accepts a USB-C cable, with CC1 and CC2 pins connected to the CYPD3177. USB data lines are broken out to a header, while the power rails are managed through a MOSFET bridge, also controlled by the CYPD3177.
When a compatible USB-C cable is connected, the CYPD3177 communicates with the power source and requests a voltage based on the DIP switch-selected reference voltage. Available options include 20V, 15V, 12V, 9V, and 5V.
Current is fixed at 2A, as requested current does not enforce actual current delivery, making adjustable current selection unnecessary. I2C connections have been removed to save space and BOM cost, as they offer little added value for this application.


<img width="990" alt="pdp_Schematic" src="https://github.com/user-attachments/assets/3d73b32f-8d03-4230-910e-fecf5c8f8b3c" />

# PCB Design

BrodBoost-PD is a 4-layer PCB measuring 11.4 mm by 54.0 mm, designed to maximize trace width, thermal performance and interfere as minimally as possible to the power lines. This layout comfortably supports the nominal device current of approximately 4-5 A @ 20V.

<img width="896" alt="Screenshot 2025-03-08 at 14 27 23" src="https://github.com/user-attachments/assets/5864e3ea-8688-4e1f-a3e3-bf9867eceb08" />


