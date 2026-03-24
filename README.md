# Carenuity-PAS-CO2-Piggyack

A Carenuity-branded piggyback PCB designed for the **Infineon XENSIV™ PAS CO₂** sensor module, with integration support for compact controller platforms such as the **ESP32-C3 Mini** ecosystem.

This board provides a practical and scalable hardware interface for PAS CO₂ sensing in smart embedded applications, rapid prototyping, and modular IoT product development.

---

## Overview

The **PAS CO₂ Piggyback** is intended to simplify interfacing the Infineon photo-acoustic spectroscopy (PAS) CO₂ sensor with compact microcontroller boards by exposing clear signal routing, power rails, and communication pins through standardized headers.

The board is developed under the **Carenuity branded ecosystem**, following a modular piggyback philosophy for reusable and scalable sensor integration.

---

## Key Features

- Supports **Infineon XENSIV™ PAS CO₂** sensor module
- Designed for **modular piggyback integration**
- Breaks out sensor communication and control signals
- Supports **I2C communication**
- Includes provision for **pull-up resistors** on I2C lines
- Compatible with compact embedded controller workflows
- Suitable for prototyping, teaching, and scalable product development

---

## Functional Signals

Based on the design, the following key signals are exposed:

- **TX**
- **RX**
- **SCL**
- **SDA**
- **PWM**
- **PSEL**
- **INT**
- **GND**
- **3V3**
- **5V**

---

## Schematic Notes

The schematic indicates:

- Header-based interconnection between the PAS CO₂ module and host controller
- Two pull-up resistors:
  - **R1 = 10kΩ**
  - **R2 = 10kΩ**
- I2C pull-ups tied to **3V3**
- Sensor interface signals routed for straightforward external controller connection

---

## Board Description

This PCB is a compact piggyback adapter carrying the Carenuity branding and intended for use with the **XENSIV PAS CO₂ concentration sensor**.

Silkscreen highlights include:

- Sensor identification
- Pin labeling
- Carenuity branding
- Version marking (**V1.1** seen on board artwork)
- Modular educational/prototyping presentation

---

## Pin Mapping Summary

### Sensor/Signal Side
- TX
- RX
- SCL
- SDA
- PWM
- PSEL
- INT
- GND
- 3V3
- 5V

### Host Header Side
The host side presents routed breakout pins for easy controller integration. Exact controller mapping should be verified against the intended MCU board before deployment.

---

## Applications

- Indoor air quality monitoring
- Smart home CO₂ sensing nodes
- Classroom and lab experiments
- IoT environmental monitoring
- Rapid embedded prototyping
- Modular sensor platform development

---

## Repository Contents

- **hardware/** → KiCad project files, fabrication outputs, and exports
- **docs/** → hardware notes, images, pinout, and revision documentation
- **firmware/** → example sketches and integration demos
- **manufacturing/** → assembly and testing guidance

---

## Recommended Power and Logic

- Primary logic interface: **3.3V**
- Check the PAS CO₂ module electrical requirements before applying **5V**
- Confirm level compatibility between the controller and sensor interface lines

---

## Getting Started

1. Open the KiCad project in the `hardware/kicad/` directory
2. Review schematic and PCB layout
3. Verify pin mapping against your host controller
4. Populate pull-up resistors where required
5. Upload a test firmware example for I2C communication
6. Validate sensor response and signal integrity

---

## Design Philosophy

This board follows the Carenuity approach of creating:

- reusable modules
- standardized sensor piggybacks
- compact embedded hardware blocks
- scalable learning-to-product hardware pathways

---

## Revision

Current visible board revision from artwork:

**V1.1**

See `docs/revision-history.md` for tracked design changes.

---

## License

This repository can use an open hardware friendly license depending on your preference.
For example:

- CERN-OHL-S
- MIT (for firmware/examples)
- CC BY 4.0 (for documentation)

---

## Author / Brand

**Carenuity**
Modular and scalable embedded hardware ecosystem
