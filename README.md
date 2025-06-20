## RP2040-with-GSM-SOM
*📄 Overview
This repository contains the schematic and block design documentation for a custom 4-layer embedded system built around the Raspberry Pi Pico (RP2040). This robust design is tailored for low-power IoT applications requiring reliable communication, data logging, and remote monitoring functionalities.

## Key Components
RP2040 (Raspberry Pi Pico W): Main controller with Wi-Fi capability.

GSM System-on-Module (AS7672S): For remote communication and data transmission.

RS485 Interface: Allows communication with Energy Meters or industrial systems.

SPI Flash (W25Q32JVSSIQ): 32Mbit memory for local data storage.

RTC (DS3231): Real-time clock for time-stamping data.

## Power Circuitry:

24V to 5V DC-DC converter (3A)

LDO regulators for 3.3V and 4V output

TP4056-based Li-ion battery charging

MT3608 Boost converter (3.3V to 5V @ 4A)

## 🔌 Power Supply Logic
Primary power from 24V DC supply.

If DC-DC 5V fails, boost converter activates to maintain operation using battery.

Li-ion battery is continuously charged during regular operation.

## 🔧 Features
#🛰️ GNSS Antenna Support for positioning or navigation modules.

## 🔄 Level Shifters for voltage compatibility between RP2040 and GSM module.

## 🔐 Optocoupler Isolation for GPIO-based input/output protection.

## 🕓 Low Power Design:

Active Transmission: ~2A

Idle Consumption: ~2–5 mA

## 📐 Block Diagram Highlights
Input/Output Protection: Opto-isolated GPIOs for safe field connections.

Connectivity: UART, I2C, SPI, TTL-to-RS485, USB Type-B for debug/power.

SIM Interface: Dual SIM slots (Nano and Micro).

Test Points: Accessible headers for all critical voltages (24V, 5V, 3V3, 4V, GND, VBAT).
