**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-10-19
**SUBJECT:** Episode Brief: TinkerNews Issue #58

Here is the detailed brief for this week’s projects from TinkerNews #58.

---

### **1. MatTris Pocket Tetris Arcade**

*   **What It Is:** A self-contained, physical, tabletop arcade console for playing a Tetris-like block game.
*   **How It Works Technically:** An Arduino-compatible controller runs the game logic. The game state and playing pieces are displayed on an LED matrix, and the player controls the game using physical buttons wired to the controller.
*   **Standout Details:** The build is documented in 21 steps, covering the enclosure, wiring, assembly, and programming. The core components are the Arduino-compatible board, an LED matrix for the display, and physical buttons.
*   **Why a Maker Cares:** This is a classic retro-gaming project that results in a finished, tangible product. The detailed, step-by-step guide makes it an accessible and satisfying build for makers who want to create a complete device.

### **2. MirrorBallBot: Raspberry Pi Robot on a Ball**

*   **What It Is:** A self-balancing robot that moves on a single large sphere instead of wheels.
*   **How It Works Technically:** Motorized rollers are in contact with the top of a large ball. A Raspberry Pi, using feedback from a camera, runs Python software to control the rollers. By spinning the rollers, the robot can move the ball underneath it, continuously adjusting to maintain balance and travel.
*   **Standout Details:**
    *   **CPU:** Raspberry Pi.
    *   **Hardware:** A custom Raspberry Pi HAT connects the electronics. The system uses a camera for feedback and motorized rollers for actuation.
    *   **Software:** Python.
    *   **Capabilities:** The robot can perform finger-following, recover from being pushed, and travel along predefined paths.
*   **Why a Maker Cares:** Ball-balancing robots are a difficult and iconic challenge in control theory and robotics. This project is a well-documented and successful implementation using accessible hardware, providing a great reference for advanced robotics builders.

### **3. Open Source ESP32 Science Tricorder**

*   **What It Is:** A handheld, open-source, multi-sensor scientific instrument in a 3D-printed cyberdeck-style enclosure.
*   **How It Works Technically:** An ESP32 serves as the central processor. It interfaces with a variety of custom and off-the-shelf sensor boards to collect environmental and scientific data, which is then processed and displayed.
*   **Standout Details:**
    *   **CPU:** ESP32.
    *   **Sensors:** Includes a microspectrometer, a magnetometer, and custom sensor boards.
    *   **Software:** The system has a Python interface and custom firmware.
    *   **Open Source:** The repository is comprehensive, including firmware, PCB layouts, 3D print files, and assembly guides.
*   **Why a Maker Cares:** This is a "dream" project for many. It's an ambitious but practical reference for building any kind of portable scientific instrument, combining electronics design, 3D printing, and embedded software into one complete, open package.

### **4. ESP32 SHT41 Temperature and Humidity Monitor**

*   **What It Is:** A compact environmental monitor.
*   **How It Works Technically:** A Sensirion SHT41 sensor measures temperature and humidity. It sends this data to an ESP32 via a simple four-wire I2C connection. The ESP32 can then output the readings to the Arduino IDE's Serial Monitor or an OLED screen.
*   **Standout Details:**
    *   **Chips:** ESP32, SHT41 sensor.
    *   **Protocol:** I2C.
    *   **Sensor Features:** The SHT41 is factory-calibrated and has low power consumption. The build is compatible with the SHT4x sensor family.
    *   **Software:** Arduino IDE.
*   **Why a Maker Cares:** It's a fundamental IoT building block. The simplicity of the I2C connection makes it a great starting point for beginners, and it provides an accurate, practical base for larger environmental sensing projects.

### **5. ESP32 Smart Bin with Fill Level Tracking**

*   **What It Is:** A "smart dustbin" that monitors its own fill level and reports data to a dashboard to optimize collection routes.
*   **How It Works Technically:** An HC-SR04 ultrasonic sensor mounted inside the bin measures the distance to the trash surface. An ESP32 processes this data to calculate the fill level. It then uses Wi-Fi to send the data and alerts via MQTT to a central dashboard.
*   **Standout Details:**
    *   **Chips/Sensors:** ESP32, HC-SR04 ultrasonic sensor.
    *   **Protocols:** Wi-Fi, MQTT.
*   **Why a Maker Cares:** This is a clear, practical, end-to-end IoT application that solves a real-world problem. It’s an excellent example project for anyone wanting to build a complete system with sensing, wireless communication, and data visualization.

### **6. ESPHome Bridge for JK-BMS Battery Data**

*   **What It Is:** A bridge that extracts live data from a JK Battery Management System (BMS) and integrates it into Home Assistant.
*   **How It Works Technically:** An ESP32 running a custom ESPHome component sits between the JK-BMS and the network. It communicates with the BMS using either UART-TTL or Bluetooth Low Energy (BLE) to read pack and cell data, then exposes it to Home Assistant.
*   **Standout Details:**
    *   **Systems:** ESPHome, Home Assistant, JK-BMS.
    *   **Protocols:** UART-TTL, BLE.
*   **Why a Maker Cares:** It unlocks valuable data trapped inside a commercial battery system without interfering with its critical safety functions. This allows for custom dashboards, alerts, and automations for DIY power projects.

### **7. ESP32 Wi-Fi to Ethernet Router**

*   **What It Is:** A small router that shares a Wi-Fi connection with devices that only have an Ethernet port.
*   **How It Works Technically:** An ESP32 connects to an existing Wi-Fi network. It is paired with a W5500 Ethernet interface chip. The ESP32's software stack creates a new, separate wired LAN and provides network services like DHCP and NAT to the connected Ethernet device.
*   **Standout Details:**
    *   **Chips:** ESP32, W5500.
    *   **Features:** Provides DHCP, NAT, and a routed mode. It also has optional WireGuard protection for security.
*   **Why a Maker Cares:** This is a powerful networking utility. It's perfect for home labs, creating isolated test networks for IoT devices, or connecting devices that can’t handle enterprise Wi-Fi portals to a network via their Ethernet port.

### **8. HaleHound CYD: Wireless Security Toolkit**

*   **What It Is:** Firmware that transforms a $7 "Cheap Yellow Display" ESP32 board into a handheld wireless security testing tool.
*   **How It Works Technically:** The HaleHound CYD firmware is flashed onto the ESP32 board, which has a built-in touchscreen. The firmware provides a graphical interface for launching over 40 different wireless security modules.
*   **Standout Details:**
    *   **Hardware:** ESP32 Cheap Yellow Display (CYD).
    *   **Features:** Browser-based flashing for easy setup, touchscreen interface. Some functions require additional radio modules.
*   **Why a Maker Cares:** It's an extremely low-cost way to build a versatile, portable wireless security tool. The ease of setup makes it accessible to a wide range of makers interested in wireless protocols.

### **9. ESP32 Audio Bridge for Vintage Beolab Speakers**

*   **What It Is:** A custom audio interface that connects modern digital audio sources to vintage Beolab speakers, which have specific signal level requirements.
*   **How It Works Technically:** An ESP32-S3 processes digital audio from a TV or network stream. The firmware performs 32-bit audio processing, careful signal attenuation, and startup muting to produce a quieter signal suitable for the speakers' inputs.
*   **Standout Details:**
    *   **Chip:** ESP32-S3.
    *   **Key Learnings:** The project write-up details challenges and solutions for Ethernet timing, power supply noise cleanup, and debugging audio task underruns in a real-time system.
*   **Why a Maker Cares:** This is a superb case study in solving a real-world audio engineering problem. The project offers valuable, practical lessons in mixed-signal design and debugging for anyone working with digital audio on microcontrollers.

### **10. ESP32 Field Camera: A Reality Check**

*   **What It Is:** A project to build and deploy a low-cost, connected field camera, with a focus on the practical challenges encountered outside the lab.
*   **How It Works Technically:** An ESP32-S3 is connected to an OV5640 camera. It captures images and communicates with an Android phone running a custom Flutter app. The app then sends the images to a cloud-based AI for analysis.
*   **Standout Details:**
    *   **Stack:** ESP32-S3, OV5640 camera, Flutter app, Cloud AI.
*   **Why a Maker Cares:** This project goes beyond the "hello world" stage. It’s a valuable dose of reality, highlighting the real-world issues of communication reliability, image quality, software boundaries, and code maintenance that arise when a project leaves the workbench.

### **11. M3-CRETE: Meter Scale 3D Paste Printing**

*   **What It Is:** An open-source reference design for a meter-scale 3D printer that uses cementitious paste (like concrete).
*   **How It Works Technically:** The project provides the mechanical designs, low-voltage interface schematics, configuration files, and a Bill of Materials (BOM) to build the machine's frame and control system.
*   **Standout Details:**
    *   **Scope:** The project explicitly covers only the mechanical and low-voltage aspects. It leaves high-risk electrical work, material science, and safety engineering to the builder.
*   **Why a Maker Cares:** This is for serious, experienced makers or teams with access to a controlled facility. It provides a documented starting point for a very ambitious project in large-scale additive manufacturing.

### **12. Self-Contained PIR Trigger for Halloween Props**

*   **What It Is:** A small, portable, 9V battery-powered motion trigger module for animatronics.
*   **How It Works Technically:** An HC-SR501 PIR sensor detects movement. Its output signal triggers a PC817 optocoupler. The optocoupler acts as an isolated switch, safely triggering the prop's control wiring without direct electrical connection. The circuit is housed in a 3D-printed enclosure.
*   **Standout Details:**
    *   **Components:** HC-SR501 PIR, PC817 optocoupler.
    *   **Power:** 9V battery.
*   **Why a Maker Cares:** It's a simple, practical, and reusable module. The use of an optocoupler is a great example of a best practice for safely interfacing different electronic systems.

### **13. Knock Activated Monster Box**

*   **What It Is:** A child-friendly Halloween prop that senses a knock on its box and triggers a servo-controlled "monster" to pop out.
*   **How It Works Technically:** An electret microphone picks up sound. The signal is amplified by a simple one-transistor amplifier circuit. An Arduino reads the amplified signal, and when it detects a peak (the knock), it commands a servo to move.
*   **Standout Details:**
    *   **Components:** Electret microphone, single transistor amplifier, Arduino, servo.
*   **Why a Maker Cares:** This is an excellent educational project. Through a fun and simple build, it teaches fundamental concepts like transistor biasing, AC coupling for audio signals, threshold detection in software, and basic servo control.

### **14. OnePage: Open Source ESP32 E-Reader**

*   **What It Is:** A complete, open-source project for building a wireless handheld e-reader.
*   **How It Works Technically:** The project is centered on a specific ESP32 C61 board. The GitHub repository provides a full suite of resources: the firmware for the ESP32, 3D-printable enclosure files, a board-specific SDK, and browser-based tools for development.
*   **Standout Details:**
    *   **Chip:** ESP32 C61.
    *   **Resources:** This is a fully-realized project with all necessary files for electronics, firmware, and mechanical assembly.
*   **Why a Maker Cares:** It’s rare to find such a complete and open project for a complex consumer device. It gives makers the ability to build, inspect, and modify every aspect of a wireless e-reader.

### **15. PYNQ-Z2 Mixed-Signal Oscilloscope**

*   **What It Is:** An open measurement platform that turns a PYNQ-Z2 FPGA board into an oscilloscope, logic analyzer, and waveform generator.
*   **How It Works Technically:** A custom PCB provides the analog front-end for the PYNQ-Z2. The FPGA on the board is programmed to handle high-speed data acquisition and processing. A desktop software client called `ngscopeclient` is used to view the data.
*   **Standout Details:**
    *   **Hardware:** PYNQ-Z2 FPGA board, custom PCB.
    *   **Features:** Dual-channel, 16-bit oscilloscope, logic analyzer connection, arbitrary waveform generator.
*   **Why a Maker Cares:** This project allows makers to build their own powerful piece of lab test equipment using a relatively accessible FPGA board. It’s a fantastic project for anyone interested in FPGAs, digital signal processing, and custom instrumentation.

### **16. RP1: Open Source Humanoid Robot Stack**

*   **What It Is:** A fully open-source, reproducible system for a humanoid robot.
*   **How It Works Technically:** This is a comprehensive repository of design files and software. It is not a kit but a complete reference design.
*   **Standout Details:**
    *   **Scope:** Includes CAD files for the structure, joint designs, schematics and PCB layouts for the electronics, firmware, control software, and machine learning tools.
*   **Why a Maker Cares:** This is a project for advanced robotics labs and highly experienced builders. Its significance lies in its completeness and openness, providing an invaluable reference for those with the fabrication and robotics expertise to tackle such a build.

### **17. Arduino Wired Ethernet with ENC28J60**

*   **What It Is:** A guide on how to connect a low-cost ENC28J60 Ethernet module to an Arduino Nano.
*   **How It Works Technically:** The module connects to the Arduino via the SPI bus. The guide highlights the critical details that often trip people up: correct SPI wiring, chip-select settings, choosing the right software library, and checking voltage levels.
*   **Standout Details:**
    *   **Hardware:** Arduino Nano, ENC28J60 module.
    *   **Protocol:** SPI.
*   **Why a Maker Cares:** This solves a common, and often frustrating, problem. It’s a practical tutorial that focuses on the specific "gotchas" of getting a very popular, cheap module to work reliably.

### **18. 16-Channel GPIO Expander for ESP32**

*   **What It Is:** A compact board that adds 16 extra GPIO channels to an ESP32 using a single I²C bus.
*   **How It Works Technically:** The board is based on the MCP23017 chip, which is an I²C GPIO expander. The board provides screw terminal connections for all 16 channels and can be daisy-chained with up to seven other modules.
*   **Standout Details:**
    *   **Chip:** MCP23017.
    *   **Protocol:** I²C.
    *   **Features:** Provides 16 channels, supports eight addressable modules, has reverse polarity protection, 5V regulation, and LEDs to indicate the board's address.
*   **Why a Maker Cares:** It directly solves one of the most common limitations in complex projects: running out of pins. This is a well-designed, practical utility board that makes it easy to add relays, buttons, and sensors.

### **19. Connect a Zehnder ComfoAir Q to Home Assistant**

*   **What It Is:** An ESPHome-based project to integrate a Zehnder ComfoAir Q ventilation unit into Home Assistant.
*   **How It Works Technically:** An ESP32 and a CAN transceiver chip are physically connected to the CAN bus on the ventilation unit. The ESP32 runs an ESPHome project that decodes CAN bus messages for ventilation data and sends commands for airflow control, exposing all of it to Home Assistant.
*   **Standout Details:**
    *   **Hardware:** ESP32, CAN transceiver.
    *   **Protocol:** CAN bus.
    *   **Systems:** ESPHome, Home Assistant.
*   **Why a Maker Cares:** It’s a perfect example of bridging a proprietary commercial appliance into an open smart home system. It also provides a practical guide to interfacing with CAN bus, a protocol common in automotive and industrial applications.

### **20. Pico2Arcade: 13 Games on a $5 Pi Pico 2**

*   **What It Is:** A minimal breadboard arcade that plays 13 classic games on a Raspberry Pi Pico 2.
*   **How It Works Technically:** The new RP2350 chip on the Pico 2 is powerful enough to handle all game logic, graphics for a small color display, sound generation for a speaker, and input from physical switches, all while maintaining a claimed 60 frames per second.
*   **Standout Details:**
    *   **Chip:** Raspberry Pi Pico 2 (RP2350).
    *   **Cost:** Around $5 for the core components.
    *   **Performance:** 60 FPS.
    *   **Software:** Code is open source on GitHub.
*   **Why a Maker Cares:** This is a stunning demonstration of the performance of the new RP2350 microcontroller. The extremely low cost and minimal hardware make it a very accessible and impressive project.

### **21. ZeroClaw: Local AI Assistant on Raspberry Pi**

*   **What It Is:** A software framework for running a self-hosted AI agent on a Raspberry Pi that can interact with hardware.
*   **How It Works Technically:** ZeroClaw is a runtime written in Rust. It takes natural-language requests and translates them into actions, interfacing with hardware through GPIO, I2C, SPI, and USB. For example, "turn on the light" could toggle a GPIO pin connected to a relay.
*   **Standout Details:**
    *   **Software:** Rust-based agent runtime.
    *   **Interfaces:** GPIO, I2C, SPI, USB.
    *   **Disclaimer:** This is a software foundation; the user must handle all wiring, AI model setup, and safety.
*   **Why a Maker Cares:** This is a toolkit for building the next generation of maker projects. It provides the software backbone for creating truly "smart" devices that can be controlled with natural language and run entirely locally.

### **22. PID Line Following Robot**

*   **What It Is:** A classic line-following robot that uses PID control for smooth and accurate movement.
*   **How It Works Technically:** A row of IR sensors reads the line on the floor. A microcontroller processes these readings to estimate the robot's position and error. A PID (Proportional-Integral-Derivative) control algorithm in the code calculates the necessary speed adjustments for the two drive motors to make constant steering corrections.
*   **Standout Details:**
    *   **Control Method:** PID feedback loop.
    *   **Components:** IR sensors, two motors.
*   **Why a Maker Cares:** This is the quintessential project for learning and visualizing closed-loop control theory. The immediate feedback of watching the robot succeed or fail to follow the line makes it a powerful educational tool.

### **23. Arduino PID Temperature Controller PCB**

*   **What It Is:** A custom PCB designed for building a precise PID temperature controller using an Arduino.
*   **How It Works Technically:** The board hosts an Arduino Nano Every. It includes circuitry for reading high-precision PT100 and PT1000 temperature sensors. The Arduino runs PID firmware and switches two 5V Solid-State Relay (SSR) outputs to control a heating element.
*   **Standout Details:**
    *   **Hardware:** Arduino Nano Every, inputs for PT100/PT1000 sensors, dual 5V SSR outputs.
    *   **Design:** KiCad files are provided for the PCB.
*   **Why a Maker Cares:** This provides a robust hardware foundation for projects needing stable and accurate temperature control, like a reflow oven or sous-vide machine. The support for PT sensors is a step up in precision from typical hobbyist thermistors.

### **24. ESP32 Motion-Controlled Snake Game**

*   **What It Is:** The classic Snake game on an ESP32, where the snake is controlled by tilting the device.
*   **How It Works Technically:** An MPU6050 gyroscope and accelerometer module is connected to an ESP32. The ESP32 reads the tilt data from the MPU6050 and uses it as directional input for the game logic. The game is displayed on a small OLED screen.
*   **Standout Details:**
    *   **Hardware:** ESP32, MPU6050 IMU, OLED display.
    *   **Software:** A complete Arduino sketch is provided.
*   **Why a Maker Cares:** A fun and simple project that combines three very popular modules. It's an excellent introduction to using an Inertial Measurement Unit (IMU) as a control input for a game or interface.