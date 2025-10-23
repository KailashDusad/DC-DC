# Non-Isolated DC-DC Converters with STM32 Control

## Overview
Design, implementation, and testing of three types of non-isolated DC-DC converters: **Buck**, **Boost**, and **Buck-Boost** converters. The converters are controlled using an STM32 microcontroller with PWM-based switching to achieve precise voltage regulation.

## Project Features

- **Three Converter Topologies**: Buck, Boost, and Buck-Boost converters for diverse voltage conversion applications
- **STM32 Microcontroller Control**: PWM-based switching control at 2.5 kHz with dynamic duty cycle adjustment
- **Real-Time Measurements**: ADC-DMA integration for continuous duty cycle control and voltage monitoring
- **Experimental Validation**: Comprehensive testing with oscilloscope analysis and comparison with theoretical calculations

## Hardware Requirements

- **Microcontroller**: STM32 development board
- **Power Supply**: DC power supply (adjustable voltage source)
- **Components**: 
  - Inductors (L)
  - Capacitors (C)
  - Diodes (D)
  - MOSFETs/IGBTs with gate drivers
  - Resistive loads
- **Measurement Tools**: 
  - Oscilloscope for waveform analysis
  - Digital multimeters for voltage/current measurements

## Software Requirements

- **STM32CubeIDE**
- **Embedded C** for firmware development

## Converter Topologies

### 1. Buck Converter (Step-Down)
Reduces input voltage to a lower output voltage
- **Duty Cycle Range**: 0 to 0.7
- **Output Voltage**: Vout = D × Vin (where D is duty cycle)
- **Operating Mode**: Continuous Conduction Mode (CCM)

### 2. Boost Converter (Step-Up)
Increases input voltage to a higher output voltage
- **Duty Cycle Range**: 0 to 0.7
- **Output Voltage**: Vout = Vin / (1 - D)
- **Operating Mode**: Continuous Conduction Mode (CCM)

### 3. Buck-Boost Converter
Provides both step-up and step-down voltage conversion with polarity reversal
- **Duty Cycle Range**: 0 to 0.7
- **Output Voltage**: Vout = -D × Vin / (1 - D)
- **Operating Mode**: Continuous Conduction Mode (CCM)

