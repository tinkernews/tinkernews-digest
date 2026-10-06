TO: Podcast Hosts
FROM: Research Editor
DATE: 2026-10-06
SUBJECT: Episode Brief for TinkerNews #56

Here is the detailed research brief for our next episode, covering TinkerNews Issue #56. I have broken down every project with the key technical details and the "so what" for our maker audience. Please stick to these facts, as they are drawn directly from the source material.

---

### **Episode 56 Brief: ESP32 in the Wild**

This week's theme is heavily focused on ESP32 projects that bridge the digital and physical worlds in practical ways, from safety devices to data consoles and home automation. We also have some great deep-dives into fundamental electronics, modular design, and open-source hardware.

---

### **Arduino Category**

#### **1. Wearable ESP32 Fall Detector Sends WhatsApp Alerts**

*   **What It Is:** A wearable device in a 3D-printed case that detects when a user falls, confirms they are immobile, and automatically sends a notification via WhatsApp.
*   **How It Works Technically:** An MPU6050 Inertial Measurement Unit (IMU) constantly monitors for sudden changes in orientation and acceleration indicative of a fall. The XIAO ESP32-S3 microcontroller analyzes this data. If a potential fall is detected, it starts a ten-second timer to check for immobility. If the user does not move, the ESP32 connects to the internet via Wi-Fi and uses the CircuitDigest Cloud service to trigger and send a pre-configured WhatsApp message to a contact.
*   **Standout Details:**
    *   **MCU:** Seeed Studio XIAO ESP32-S3
    *   **Sensor:** MPU6050 (6-axis accelerometer and gyroscope)
    *   **Protocol/Service:** Wi-Fi, CircuitDigest Cloud for WhatsApp integration.
    *   **Enclosure:** Includes files for a 3D-printed case.
*   **Maker Angle:** This is a complete, real-world assistive technology project. Makers will be interested in the practical application of an IMU for event detection beyond simple orientation. It's a great example of using a third-party cloud service to easily integrate with a major messaging platform like WhatsApp, bypassing more complex API integrations. The project also forces a discussion of real-world limitations like network connectivity, sensor calibration, and managing false alarms.

#### **2. Wall-Mounted ESP32 Touchscreen with Wireless Relay Control**

*   **What It Is:** A home automation control panel with a touchscreen that wirelessly communicates with a separate board to control relays and display sensor data.
*   **How It Works Technically:** The system uses two ESP32s. The first is a VIEWE ESP32-S3 with an integrated touchscreen, which serves as the wall-mounted user interface. The second ESP32 is connected to a four-relay module and a DHT22 temperature/humidity sensor. The two boards communicate directly with each other using the ESP-NOW protocol, which eliminates the need for a physical data cable or reliance on a central Wi-Fi router for their link. The entire system is managed by ESPHome, which also pulls in external data: weather forecasts from OpenWeather, UV data from Open-Meteo, and time from an NTP server.
*   **Standout Details:**
    *   **MCUs:** Two ESP32 boards, one is a VIEWE ESP32-S3 touchscreen.
    *   **Protocol:** ESP-NOW for board-to-board communication.
    *   **Sensor:** DHT22 (temperature and humidity).
    *   **Software Stack:** ESPHome.
    *   **External Data:** Integrates with OpenWeather, Open-Meteo, and NTP APIs.
*   **Maker Angle:** The key takeaway here is ESP-NOW. It’s a powerful protocol for creating responsive, local device-to-device communication without bogging down a Wi-Fi network. This project demonstrates a clean, decentralized hardware architecture. It's also a practical tutorial on building a sophisticated user interface with ESPHome that aggregates both local sensor data and multiple internet-based APIs into one display.

#### **3. Build an ESP32 Aircraft Radar Console**

*   **What It Is:** A standalone, desktop device with a screen that displays nearby aircraft locations, functioning as a personal ADS-B data console.
*   **How It Works Technically:** An ESP32 uses its Wi-Fi capability to connect to the internet and query the OpenSky public API for aircraft telemetry data. It then processes this data and renders it on a 1.8-inch TFT display. The firmware, named FlyRadar32, is installed using a browser-based tool. The software includes logic for resiliently handling telemetry and has additional screens for weather and diagnostics.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **Display:** 1.8-inch TFT.
    *   **Data Source:** OpenSky API.
    *   **Software:** Custom firmware (FlyRadar32) with browser-based installation.
    *   **Enclosure:** Includes a FreeCAD design for a 3D-printed case.
*   **Maker Angle:** This is a classic "data appliance" project. It shows makers how to create a dedicated physical interface for a specific data stream, turning abstract online information into a tangible, at-a-glance display. The browser-based firmware install is a user-friendly touch. It’s a great project for anyone interested in aviation, APIs, and creating polished, finished-looking electronics.

#### **4. Arduino Five-Antenna Selector Uses CAT and BCD**

*   **What It Is:** An automated controller for amateur radio operators that selects one of five different antennas based on the frequency band being used.
*   **How It Works Technically:** An Arduino microcontroller listens for input from radio equipment. It can accept this input in two formats: CAT serial data or BCD (Binary-Coded Decimal) signals. Based on the received band information, the Arduino activates a corresponding relay to switch the correct antenna into the circuit. The selected antenna is shown on a seven-segment display, and a buzzer sounds to alert the operator of the change.
*   **Standout Details:**
    *   **MCU:** Arduino.
    *   **Input Protocols:** CAT (Computer Aided Transceiver) serial and BCD.
    *   **Outputs:** Relay control for 5 antennas, a seven-segment display, a buzzer.
*   **Maker Angle:** This solves a very specific, practical problem for a technical hobby (ham radio). It’s an excellent example of interfacing with specialized equipment protocols (CAT and BCD). For general makers, it demonstrates robust input handling from multiple sources and provides a clear logic flow: read input, make a decision, activate outputs, and provide user feedback.

#### **5. Use a BJT to Drive a 12V MOSFET from Arduino**

*   **What It Is:** A fundamental circuit demonstrating how to safely control a high-current, high-voltage device (like a 12V motor) from a low-voltage, low-current microcontroller pin (like a 5V Arduino).
*   **How It Works Technically:** A 5V signal from an Arduino pin is not sufficient to fully turn on a typical 12V MOSFET. This circuit uses a Bipolar Junction Transistor (BJT) as an intermediate stage. The Arduino's 5V signal turns on the BJT, which then acts as a switch to pull the MOSFET's gate to ground or connect it to the 12V supply, fully turning the MOSFET on or off. The MOSFET then handles switching the heavy current for the 12V load, isolating the microcontroller from the high-power circuit.
*   **Standout Details:**
    *   **Voltages:** 5V logic level (Arduino) controlling a 12V load circuit.
    *   **Components:** BJT (Bipolar Junction Transistor), MOSFET (Metal-Oxide-Semiconductor Field-Effect Transistor).
    *   **Function:** Level-shifting and current amplification.
*   **Maker Angle:** This is a must-know circuit for any maker moving beyond blinking LEDs. It explains *why* you can't just connect a motor to a GPIO pin. Understanding this BJT/MOSFET driver arrangement is the gateway to controlling motors, solenoids, large LED strips, relays, and fans safely and effectively. It’s a core building block of physical computing.

#### **6. Build an Uno with a Built-In MPU-6050**

*   **What It Is:** A custom-designed PCB, created in KiCad, that integrates an Arduino Uno R3 layout with an onboard MPU-6050 IMU sensor.
*   **How It Works Technically:** The design combines the standard SMD-compatible footprint of an Arduino Uno R3 with the circuitry for an MPU-6050. It includes the necessary logic-level shifting to handle I²C communication between the 5V ATmega microcontroller and the 3.3V MPU-6050 sensor. The MPU-6050 is physically placed on the underside of the PCB to save space.
*   **Standout Details:**
    *   **MCU:** Arduino Uno R3 compatible (SMD).
    *   **Sensor:** MPU-6050 (6-axis IMU).
    *   **Protocol:** I²C with 5V to 3.3V level shifting.
    *   **Software:** KiCad (for the PCB design).
*   **Maker Angle:** This project is about custom PCB design for integration and compactness. For makers who are tired of dealing with breakout boards, messy jumper wires, and mounting issues, this shows the next step: designing your own application-specific board. It’s a perfect case study in combining a microcontroller and a common sensor onto a single, clean PCB, which is a key skill for creating professional, repeatable projects.

---

### **DIY Electronics Category**

#### **7. FaderBuddy Makes Motorized Faders Modular**

*   **What It Is:** A small control board that turns a standard motorized fader into a smart, modular I²C peripheral.
*   **How It Works Technically:** An ATtiny1616 microcontroller is dedicated to managing a single 60mm motorized slider. This board handles all the low-level motor driving and position sensing. It presents a simple I²C interface to a host microcontroller. The host can then command the fader by reading its current position, setting a target position for the motor to move to, and even implementing "virtual" features like detents or haptic feedback patterns. Multiple FaderBuddy boards can be connected to the same I²C bus.
*   **Standout Details:**
    *   **MCU:** ATtiny1616.
    *   **Component:** 60 mm motorized fader.
    *   **Protocol:** I²C.
    *   **Features:** Virtual detents, haptic feedback.
*   **Maker Angle:** This is a brilliant example of distributed control and modular design. It abstracts away a complex task (driving a motorized fader) into a simple-to-use component. Makers building custom control surfaces, audio mixers, or automation panels no longer need to write tricky timing and motor control code themselves. They can just treat the fader like any other I²C sensor or device, which dramatically simplifies complex projects with many moving parts.

#### **8. Build a $10 ESP32 Flock Camera Detector**

*   **What It Is:** A low-cost, portable device that passively listens for Wi-Fi signals characteristic of Flock Safety automated license plate reader cameras.
*   **How It Works Technically:** An ESP32 is put into a mode where it can monitor Wi-Fi traffic without connecting to any network. It analyzes nearby Wi-Fi packets, looking for specific signatures that have been documented as being associated with Flock Safety cameras. If a match is found, it can provide a configurable alert. The project is solderless, can be built on a custom PCB, and supports GPS for mapping detections.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **Cost:** $9–$11.
    *   **Connectivity:** Wi-Fi (passive monitoring).
    *   **Features:** Solderless build option, optional GPS mapping, configurable alerts.
*   **Maker Angle:** This project sits at the intersection of citizen science, privacy, and hardware. It’s a hands-on demonstration of passive Wi-Fi analysis. Makers will learn how network devices can be identified by their traffic patterns, even without connecting to them. It's a very accessible entry point into network monitoring and raises important discussions about public surveillance, privacy, and the legality of wireless monitoring.

#### **9. Project Hydra: An Open 1 W LoRa PCB for Meshtastic**

*   **What It Is:** An open-source KiCad PCB design for a simple, high-power (1 Watt) LoRa communications board specifically intended for the Meshtastic network.
*   **How It Works Technically:** This is not a finished product, but a set of design files. The repository contains the schematic and PCB layout for a minimal board capable of 1W LoRa transmission. It’s designed to be used with Meshtastic, an open-source, off-grid, decentralized messaging project.
*   **Standout Details:**
    *   **Technology:** LoRa.
    *   **Power:** 1 Watt.
    *   **Software:** KiCad (design files), intended for Meshtastic.
    *   **License:** GPL-3.0.
*   **Maker Angle:** This is purely for the advanced maker interested in RF and custom PCB design. The value is that it's an open, editable reference design for a high-power LoRa board. Makers can study it to understand the design principles of RF layouts, or they can adapt it for their own custom Meshtastic nodes. It’s a starting point for building powerful, long-range communication hardware, with the caveat that they must check regulations for 1W transmission.

---

### **ESP32 Category**

#### **10. A Gesture-Controlled ESP32 Glove for 3D Building**

*   **What It Is:** "Aloft" is a glove-based input device that allows a user to perform 3D modeling and building on a phone or in a browser using hand gestures.
*   **How It Works Technically:** The glove is equipped with MPU-6050 IMU sensors to track hand motion and orientation. Two ESP32 boards process the sensor data and transmit it via Bluetooth to a paired phone or computer. The user can tilt their hand to move an object along the X, Y, or Z axes, and use pointing and tapping gestures to place or modify shapes within the 3D application.
*   **Standout Details:**
    *   **MCUs:** Two ESP32 boards.
    *   **Sensors:** MPU-6050 IMUs.
    *   **Protocol:** Bluetooth.
    *   **Application:** A custom 3D building app for browser and iPhone.
*   **Maker Angle:** This is a sophisticated human-computer interface (HCI) project. It demonstrates how to combine multiple sensors and microcontrollers to capture complex, nuanced human movement. The use of Bluetooth to create a wireless controller for a mobile app is a very relevant skill set. It’s an inspiring project for anyone interested in wearables, virtual reality, or creating novel input devices.

#### **11. Build an ESP32-S3 Bambu Lab Printer Monitor**

*   **What It Is:** A small, standalone device with a color screen that sits next to a Bambu Lab 3D printer and displays its real-time status.
*   **How It Works Technically:** An ESP32-S3 connects to the same network as the Bambu Lab printer. Using the MQTT protocol, it subscribes to the printer's status topics over either the local LAN or the cloud service. It displays key information like temperatures, print progress, and events on an ST7789 TFT screen. Setup is done through a web browser, and an optional buzzer can provide audible alerts.
*   **Standout Details:**
    *   **MCU:** ESP32-S3.
    *   **Display:** ST7789 TFT.
    *   **Protocol:** MQTT.
    *   **Connectivity:** LAN or Cloud connection options.
    *   **Features:** Browser-based setup, optional buzzer.
*   **Maker Angle:** Similar to the aircraft radar, this is another great "data appliance" project, but this time using MQTT, which is the cornerstone of modern IoT. Makers will learn how to tap into the data stream of a commercial smart device and create a custom, dedicated monitor. It highlights the power of local network communication (LAN mode) for speed and privacy, and provides a clear example of a practical, useful tool for a popular maker hobby.

#### **12. How FlipDeFlock Maps Nearby Surveillance Signals**

*   **What It Is:** A project that uses a Flipper Zero and an ESP32 to passively detect and identify various types of surveillance equipment.
*   **How It Works Technically:** The ESP32 does the heavy lifting of passive wireless listening. It scans for Wi-Fi probe requests to identify cameras that use randomized MAC addresses by their fingerprints. It also listens for other signals like Remote ID (used by drones) and Bluetooth Low Energy (BLE) broadcasts to gather more context about nearby devices. The Flipper Zero likely acts as the user interface and controller for the ESP32 module. The results are presented as clues, not certainties.
*   **Standout Details:**
    *   **Hardware:** Flipper Zero paired with an ESP32.
    *   **Techniques:** Passive listening, probe-request fingerprinting.
    *   **Signals Detected:** Wi-Fi, Remote ID, BLE.
*   **Maker Angle:** This is an advanced version of the Flock detector, showcasing a multi-faceted approach to wireless intelligence gathering. For makers interested in security and RF, this is a deep dive. It demonstrates that you can identify devices by *how* they talk, not just *what* they say. It’s a lesson in digital forensics and the fact that even with technologies like MAC randomization, devices can still leak identifiable information.

---

### **Other Categories (Quick Hits)**

#### **13. [IoT] WiFi Sensing Turns Routers Into Room Monitors**

*   **What It Is:** "RuView" is an open-source project that uses a Wi-Fi router's signals to sense human presence and activity in a room without cameras.
*   **How It Works Technically:** It analyzes disturbances and reflections in existing Wi-Fi radio waves to estimate metrics like presence, movement, breathing rate, and even heart rate. It does not require any wearable devices on the person being monitored. The project includes visualization tools and smart-home integration.
*   **Maker Angle:** This is a look at the cutting edge of sensor technology, treating Wi-Fi not just as a data pipe, but as an active sensing medium. While the hardware support is likely limited, it introduces makers to the concept of Channel State Information (CSI) and the possibilities of device-free sensing. It's a high-concept project that could spark ideas about privacy-preserving monitoring.

#### **14. [Raspberry Pi] Build a Raspberry Pi MQTT Hub with Mosquitto**

*   **What It Is:** A guide to setting up a Raspberry Pi as a central MQTT server (a "broker") for a local network of smart devices.
*   **How It Works Technically:** The guide walks through installing and securing the Mosquitto MQTT broker software on a Raspberry Pi. Once running, IoT devices like ESP32s or Shelly products can publish data to the Pi and subscribe to data from it. This creates a central hub for communication, so devices don't need to know about each other directly. The guide mentions using MQTT Explorer to monitor traffic.
*   **Maker Angle:** This is a foundational project for anyone serious about home automation. Setting up a local MQTT broker is the key to creating a robust, private, and interoperable smart home. It allows devices from different brands to communicate seamlessly and integrates perfectly with tools like Home Assistant and Node-RED. It moves a maker from simple point-to-point projects to a true, networked ecosystem.

#### **15. [3D Printing] Set Up Automatic Multi-Color Printing on a QIDI Q2**
*   **What It Is:** A walkthrough for configuring a QIDI Q2 3D printer for automated multi-color printing using an add-on system.
*   **How It Works:** The system uses a box that holds four different spools of filament. The QIDI Studio slicing software is used to assign colors to different parts of a model and generate the necessary G-code for filament changes. During the print, the printer will automatically unload the current filament, purge the nozzle in a "waste tower," and load the next color as needed. The guide covers the full process from wiring and drying filament to handling failed changes.
*   **Maker Angle:** For 3D printing enthusiasts, this demystifies the process of multi-material printing. It's a practical guide that not only shows the "happy path" but also addresses common, real-world problems like waste material, material compatibility, and how to recover from a failed filament change mid-print, which is invaluable information for anyone attempting long, complex prints.