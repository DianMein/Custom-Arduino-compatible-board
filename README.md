# Custom Arduino-Compatible Development Board

## Overview

This project is an **open-source Arduino-compatible development board**
designed from scratch to provide a **compact, versatile, and IoT-ready
platform** for embedded systems and electronics development.

Built for **hobbyists, students, and professionals**, this board
combines the familiarity of the Arduino ecosystem with **modern hardware
features** like **USB-C**, **Li-ion battery support**.

------------------------------------------------------------------------

## Features

### 1. Microcontroller

-   **ATmega32U4** (Arduino Leonardo compatible)
    -   8-bit AVR @ 16 MHz
    -   Native USB for programming and HID support
    -   32 KB Flash, 2.5 KB SRAM, 1 KB EEPROM

### 2. Connectivity

-   **USB-C** programming interface
-   **UART, I²C, SPI** communication buses

### 3. Power Management

-   **USB-C powered** (5V input)
-   **Li-ion battery support** with onboard charging circuit (MCP73831)
-   **3.3V and 5V regulators** for mixed-voltage peripherals

### 4. Peripherals

-   14x Digital I/O pins
-   6x ADC channels (10-bit resolution)
-   PWM on 6 pins
-   User-programmable RGB LED
-   Reset and Boot buttons
-   Onboard status LEDs (Power, TX/RX)

------------------------------------------------------------------------

## Technical Specifications

  **Feature**         **Specification**
  ------------------- --------------------------------
  MCU                 ATmega32U4
  Clock Speed         16 MHz
  Flash Memory        32 KB
  SRAM                2.5 KB
  EEPROM              1 KB
  USB                 Native USB-C
  Operating Voltage   5V / 3.3V
  I/O Pins            14 Digital, 6 Analog
  Communication       UART, SPI, I²C
  Power Options       USB-C, Li-ion battery
  Dimensions          \~50mm x 25mm (compact design)

------------------------------------------------------------------------

## Applications

-   IoT sensor nodes
-   Home automation systems (MQTT, Home Assistant)
-   Robotics and motor control
-   Wearable electronics
-   Educational embedded systems

------------------------------------------------------------------------

## Getting Started

### **Step 1: Install Arduino IDE**

-   [Download Arduino IDE](https://www.arduino.cc/en/software)

### **Step 2: Add Board to Arduino IDE**

-   Select **Arduino Leonardo** under **Tools → Board**
-   Choose the correct **COM port**

### **Step 3: Upload Your First Program**

``` cpp
// Simple Blink Demo
const int LED = 13;

void setup() {
  pinMode(LED, OUTPUT);
}

void loop() {
  digitalWrite(LED, HIGH);
  delay(500);
  digitalWrite(LED, LOW);
  delay(500);
}
```

------------------------------------------------------------------------

## Repository Structure

    Custom-Arduino-Board/
    ├── hardware/          # KiCad project, schematics, PCB layout
    ├── firmware/          # Arduino bootloader + example sketches
    ├── docs/              # PDF schematics, BOM, and datasheets
    ├── images/            # PCB renders and block diagrams
    └── README.md          # Project documentation

------------------------------------------------------------------------

## Future Enhancements

-   **ESP32-S3 integration** → Wi-Fi + BLE onboard
-   **MicroSD storage** → Data logging
-   **Low-power modes** → Battery optimization
-   **Dedicated Arduino core package** for seamless IDE support

------------------------------------------------------------------------

## License

This project is licensed under the **GNU General Public License v2.0
(GPL-2.0)**.

------------------------------------------------------------------------

## Author

**Dian Meintjes**\
*Embedded Electronics & PCB Design Enthusiast*\
