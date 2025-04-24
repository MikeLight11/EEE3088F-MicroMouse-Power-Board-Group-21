# Micromouse Power Subsystem

## Overview
This repository contains the design files and documentation for the power subsystem of a micromouse robot developed for the EEE3088F 2025 course project. The micromouse is an autonomous robot designed to navigate through and solve mazes efficiently. The power subsystem is responsible for powering the entire micromouse, including battery management, motor control, and regulated power distribution.

## Project Description
The micromouse project consists of four main modules:
- Motherboard (provided)
- Processor (provided)
- Sensing system (provided)
- Power subsystem (this project)

Our power subsystem is designed to meet the following key requirements:
- Power and control 4 motors bidirectionally
- Provide battery monitoring via INA219 on I2C bus
- Charge the battery from 9V input with dual charging modes
- Integrate USB-C with 9V output
- Provide external load switching capabilities
- Deliver regulated 3.3V and 5V outputs
- Include ON/OFF switch with ultra-low power standby mode

## Features
- **Battery Management**: Uses BQ24074 charge controller for efficient Li-Ion battery charging with configurable charging currents (200mA standard, 600mA fast charging)
- **Motor Control**: H-bridges for bidirectional control of up to 4 motors
- **Power Regulation**: Provides stable 3.3V and 5V power rails
- **Load Switching**: Two external load switches capable of handling 1A each
- **Battery Monitoring**: INA219 current/voltage monitoring over I2C
- **Power-saving Mode**: <30μA current draw in OFF state
- **USB-C Integration**: Supports power input through USB-C

## Repository Structure
- `/Docs` - Documentation including the report
- `/Final Schematic and PCB` - KiCad schematic files and PCB design files
- `/Footprint Library` - Contains all imported footprints 
- `/Gerbers` - Production Gerber files
- `/Old Schematics` - Backup KiCad schematic files 
- `/Production files` - Contains the zip file of the Gerbers, the BOM and CPL (JLCPCB Submission files)

## Hardware Specifications
- Dimensions: Maximum 82mm × 60mm
- Battery: 3.7V 800mAh LiPo
- Input Voltage: 9V or USB-C
- Output Voltages: 3.3V (300mA max) and 5V (1.5A max)
- PCB Connector: 2x16 (2.54mm pin pitch) header connecting to the motherboard

## Contributors
- Michael Lighton (LGHMIC003)
- Michael Smith (SMTMIC078)

## Acknowledgments
- University of Cape Town, Department of Electrical Engineering
- EEE3088F course staff
