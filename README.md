# Carenuity-PAS-CO2-Piggyack

A Carenuity-branded piggyback PCB designed for the **Infineon XENSIV™ PAS CO₂** sensor module, with integration support for compact controller platforms such as the **ESP32-C3 Mini** ecosystem.

This board provides a practical and scalable hardware interface for PAS CO₂ sensing in smart embedded applications, rapid prototyping, and modular IoT product development.


## Overview

The **PAS CO₂ Piggyback** is intended to simplify interfacing the Infineon photo-acoustic spectroscopy (PAS) CO₂ sensor with compact microcontroller boards by exposing clear signal routing, power rails, and communication pins through standardized headers.

The board is developed under the **Carenuity branded ecosystem**, following a modular piggyback philosophy for reusable and scalable sensor integration.


## Key Features

- Supports **Infineon XENSIV™ PAS CO₂** sensor module
- Designed for **modular piggyback integration**
- Supports **I2C communication**
- Includes provision for **pull-up resistors** on I2C lines
- Compatible with compact embedded controller workflows
- Suitable for prototyping, teaching, and scalable product development


## Schematic Notes

The schematic:

- Header-based interconnection between the PAS CO₂ module and host controller
- Two pull-up resistors:
  - **R1 = 10kΩ**
  - **R2 = 10kΩ**
- I2C pull-ups tied to **3V3**
- Sensor interface signals routed for straightforward external controller connection


# Pinout Reference

## Main Interface Signals

| Signal | Function |
|--------|----------|
| TX     | UART transmit / sensor communication line |
| RX     | UART receive / sensor communication line |
| SCL    | I2C clock |
| SDA    | I2C data |
| PWM    | PWM signal output/interface |
| PSEL   | Protocol or interface selection line |
| INT    | Interrupt output |
| GND    | Ground reference |
| 3V3    | 3.3V rail |
| 5V     | 5V rail |

## Pull-up Network

| Ref | Value | Purpose |
|-----|-------|---------|
| R1  | 10kΩ  | I2C pull-up |
| R2  | 10kΩ  | I2C pull-up |

# Hardware Overview

The PAS CO₂ Piggyback is a dedicated adapter/interface board for the Infineon XENSIV PAS CO₂ module.

## Functional Intent

The board is meant to:

- host or align with the PAS CO₂ sensor module
- expose usable external connection points
- simplify controller wiring
- maintain consistency within the Carenuity piggyback hardware ecosystem

## Interface Style

The board uses dual header arrangements for signal breakout. The labeling suggests compatibility with compact embedded control boards, particularly development boards used in sensor prototyping.

## Notable Design Elements

- Clear signal silkscreen
- Carenuity visual identity
- PAS CO₂ product labeling
- I2C pull-up resistor provision
- Compact rectangular piggyback layout
- Version-controlled board artwork

## Integration Considerations

Before deployment, verify:

- logic voltage compatibility
- actual PAS CO₂ module pin function
- whether UART, I2C, or PWM is the intended active interface
- power supply rail requirements
- mechanical clearance for the mounted module
## Applications

- Indoor air quality monitoring
- Smart home CO₂ sensing nodes
- Classroom and lab experiments
- IoT environmental monitoring
- Rapid embedded prototyping
- Modular sensor platform development

## Recommended Power and Logic

- Primary logic interface: **3.3V**
- Check the PAS CO₂ module electrical requirements before applying **5V**
- Confirm level compatibility between the controller and sensor interface lines



## Design Philosophy

This board follows the Carenuity approach of creating:

- reusable modules
- standardized sensor piggybacks
- compact embedded hardware blocks
- scalable learning-to-product hardware pathways


## Revision

Current visible board revision from artwork:

**V1.1**

