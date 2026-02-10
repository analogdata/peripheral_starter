# AD - Peripheral Starter Board

A versatile peripheral development board designed for microcontroller projects, providing commonly used input/output components for rapid prototyping and learning.

**Status:** Design in Progress
**Version:** v1
**Date:** 2026-02-10
**EDA Tool:** KiCad 9.0

## Overview

The Peripheral Starter Board is an expansion board that provides a variety of peripheral components commonly used in embedded systems development. It is designed to interface with microcontroller development boards, offering ready-to-use circuits for sensors, actuators, and user interface components.

## Features

### Input Peripherals
- **4x Push Button Switches** - Tactile switches for user input
- **Potentiometer** - Analog input for variable resistance/voltage readings
- **LDR (Light Dependent Resistor)** - Light sensing for ambient light detection

### Output Peripherals
- **4x LEDs** - Standard indicator LEDs with current limiting resistors (330 ohm)
- **WS2812B RGB LED** - Addressable RGB LED for colorful visual feedback
- **Piezo Buzzer** - Audio output with transistor driver (BC547)

### Display Interface
- **OLED SSD1306 Connector** - I2C interface for 128x64 OLED display module

### Timekeeping
- **RTC Circuit Connector** - Interface for Real-Time Clock modules

### Power Management
- **5V Input** - Main power input from controller board
- **3.3V Regulated Output** - AMS1117-3.3 linear voltage regulator
- **Power Jumper Shunt** - Selectable power source from controller

## Schematic Sections

| Section | Description |
|---------|-------------|
| LED Circuit | 4 LEDs with 330 ohm current limiting resistors |
| Switches Circuit | 4 push buttons with pull-up/pull-down configuration |
| Potentiometer Circuit | Analog voltage divider circuit |
| LDR Circuit | Light sensor with voltage divider |
| RGB (WS2812B) Circuit | Addressable LED with decoupling capacitor |
| Buzzer Circuit | Piezo buzzer with BC547 transistor driver |
| OLED SSD1306 Circuit | I2C connector for OLED display |
| RTC Circuit | Connector for RTC module interface |
| 3.3V Power Supply | AMS1117-3.3 with input/output capacitors |

## Bill of Materials (Key Components)

| Reference | Component | Value/Part |
|-----------|-----------|------------|
| U1 | Voltage Regulator | AMS1117-3.3 |
| Q1 | NPN Transistor | BC547 |
| D1-D4 | LED | Standard LED |
| D5 | RGB LED | WS2812B |
| R1-R4 | Resistor | 330 ohm |
| R12, R16 | Resistor | 4.7k ohm |
| R14 | Resistor | 10k ohm |
| C1-C8 | Capacitor | 100nF / 0.1uF |
| J1-J11 | Connectors | Pin Headers (2-6 pins) |
| - | Buzzer | Piezo Buzzer |
| - | LDR | LDR07 |
| - | Potentiometer | 10k (typical) |
| - | Switches | 4x Tactile Push Buttons |
| - | Slide Switch | SPDT Slide Switch |

## Connectors

- **J4** - 6-pin Controller Interface
- **J5, J7** - 2-pin Power/Signal Connectors
- **J10, J11** - 5-pin I2C/SPI Connectors (OLED, RTC)
- **J3, J1** - 4-pin Peripheral Connectors
- **J2** - 3-pin Buzzer/RGB Connector

## Getting Started

1. **Power Supply**: Connect 5V power through the main connector or use the power jumper to receive power from the controller board
2. **Controller Interface**: Connect to your microcontroller via the pin headers
3. **Test Components**: Use the provided test points to verify functionality

## Design Files

- `peripheral_Starter.kicad_sch` - Schematic file
- `peripheral_Starter.kicad_pcb` - PCB layout file
- `peripheral_Starter.kicad_pro` - KiCad project file
- `Peripheral_Starter_v1.pdf` - Schematic PDF export

## Requirements

- KiCad 9.0 or later to open and edit design files

## Project Structure

```
peripheral_Starter/
├── peripheral_Starter.kicad_pro    # Project file
├── peripheral_Starter.kicad_sch    # Schematic
├── peripheral_Starter.kicad_pcb    # PCB layout
├── peripheral_Starter.kicad_prl    # Local project settings
├── fp-info-cache                   # Footprint cache
├── Peripheral_Starter_v1.pdf       # Schematic export
└── peripheral_Starter-backups/     # Design backups
```

## License

This project is open source hardware.

## Author

Analog Data
Website: [https://analogdata.io](https://analogdata.io)
