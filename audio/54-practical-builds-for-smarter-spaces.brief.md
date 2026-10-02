**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-09-21
**SUBJECT:** Episode Brief: TinkerNews #54 - Practical Builds for Smarter Spaces

Here is the detailed research brief for the projects covered in TinkerNews #54. All details are drawn exclusively from the source material.

---

### **ESP32**

#### 1. ESP32 MAX30102 Vital Signs Sensor
*   **What It Is:** A fingertip sensor that provides experimental readings for heart rate, SpO2 (blood oxygen saturation), and temperature.
*   **How It Works Technically:** An ESP32 microcontroller communicates with a MAX30102 sensor module over the I2C protocol. The MAX30102 performs optical sensing on a fingertip to gather the raw physiological data. The ESP32 processes this data using provided Arduino sketches to derive the three values.
*   **Standout Details:**
    *   **MCU:** ESP32
    *   **Sensor:** MAX30102 module
    *   **Protocol:** I2C
    *   **Software:** Arduino sketches
    *   **Data Points:** Heart rate, SpO2, temperature
*   **Why Makers Care:** This is a direct, hands-on introduction to acquiring physiological data. It's a great project for learning about I2C communication with a sophisticated sensor, but the source explicitly states it is not for medical diagnosis.

#### 2. ESP32 Cooker Whistle Counter
*   **What It Is:** A device that listens for and counts the whistles from a pressure cooker, then sends a notification when a target count is reached.
*   **How It Works Technically:** A MAX4466 microphone module detects sound events. The ESP32 firmware counts these events. Upon reaching a pre-selected count, the ESP32 uses its Wi-Fi connection to trigger a WhatsApp message notification via the CircuitDigest Cloud service.
*   **Standout Details:**
    *   **MCU:** ESP32
    *   **Sensor:** MAX4466 microphone
    *   **Connectivity:** Wi-Fi
    *   **Service:** CircuitDigest Cloud for WhatsApp notifications
*   **Why Makers Care:** It solves a common, real-world kitchen problem using simple event detection (sound). It’s a practical example of integrating a physical sensor with a cloud notification service. The project requires careful calibration.

#### 3. ESP32 Touchscreen Sonos Wall Panel
*   **What It Is:** A dedicated wall- or desk-mounted touchscreen remote for controlling a Sonos sound system, called SonosESP.
*   **How It Works Technically:** An ESP32-P4 microcontroller drives a 4-inch or 7-inch touchscreen. The SonosESP software browses music libraries, controls speakers, and displays album art, lyrics, weather, and a clock. Firmware can be updated without removing the device from its mounting.
*   **Standout Details:**
    *   **MCU:** ESP32-P4
    *   **Display:** 4-inch or 7-inch touchscreen
    *   **Software:** SonosESP
*   **Why Makers Care:** This is a polished, high-level user interface project that goes beyond simple blinking lights. It showcases the graphical capabilities of the newer ESP32-P4 and creates a permanent, useful smart home fixture.

#### 4. ESP32 Tesla BLE Control with Home Assistant
*   **What It Is:** A local bridge that uses an ESP32 to control and monitor a Tesla vehicle over Bluetooth Low Energy, integrating it into Home Assistant.
*   **How It Works Technically:** The ESP32 runs ESPHome firmware, configured with a provided YAML example. It communicates directly with the car using the vehicle’s BLE protocol. This brings charging controls, vehicle data, and diagnostics into a Home Assistant dashboard without relying on Tesla's cloud API.
*   **Standout Details:**
    *   **MCU:** ESP32
    *   **Protocol:** Bluetooth Low Energy (BLE)
    *   **Software Stack:** ESPHome, Home Assistant
*   **Why Makers Care:** It’s a prime example of a "local-first" IoT solution for a major product. It enhances privacy and reliability by keeping communication nearby. The source stresses the importance of security when dealing with commands that can physically affect a car.

#### 5. Replace a RIKA Stove Dongle with ESP32-S3
*   **What It Is:** An open-source project, Open Firenet, that replaces the proprietary RIKA Firenet 2.0 dongle for pellet stoves.
*   **How It Works Technically:** An ESP32-S3 board connects directly to the stove's USB port. It communicates using the stove's native USB protocol, effectively emulating the original dongle. It then provides Wi-Fi connectivity, a local web page for control, and a REST API, bypassing the manufacturer's cloud service.
*   **Standout Details:**
    *   **MCU:** ESP32-S3
    *   **Protocol:** USB (for stove communication)
    *   **Interface:** Wi-Fi, local web page, REST API
*   **Why Makers Care:** This is a classic "de-clouding" project that gives a user local, open control over their appliance. It’s an advanced project that involves reverse-engineered protocols and interfacing with a potentially dangerous appliance, highlighting real-world risks.

#### 6. RuView: WiFi Sensing Through Walls
*   **What It Is:** A system named RuView that uses Wi-Fi signals for camera-free motion and presence detection.
*   **How It Works Technically:** Multiple ESP32 nodes act as sensors, analyzing disruptions and changes in the ambient Wi-Fi signals within a room. This data is processed locally to estimate presence, movement, breathing rate, and heart rate. It provides live displays and can be linked to home-automation systems.
*   **Standout Details:**
    *   **Sensing Nodes:** ESP32
    *   **Technique:** Wi-Fi sensing
    *   **Data Derived:** Presence, movement, breathing, heart rate
*   **Why Makers Care:** This explores a cutting-edge sensing method that offers a privacy-preserving alternative to cameras for smart home applications. The project's success is noted to be highly dependent on physical room layout, calibration, and potential signal interference.

### **3D Printing**

#### 7. Open-Source RP2040 Logic IC Tester
*   **What It Is:** A piece of open-source benchtop test equipment, the OD-PT74, for testing 74xx series logic chips.
*   **How It Works Technically:** The device is controlled by a Raspberry Pi RP2040 microcontroller. It has sockets to accept 14-, 16-, and 20-pin 74xx TTL and CMOS chips. A user selects test modes via a rotary encoder and views results on an OLED display. The enclosure is 3D-printed.
*   **Standout Details:**
    *   **MCU:** RP2040
    *   **Chips Tested:** 14/16/20-pin 74xx TTL and CMOS
    *   **UI:** OLED display, rotary encoder
    *   **Open Source:** Complete PCB files and editable 3D enclosure files are provided.
*   **Why Makers Care:** This is a complete, reproducible workshop tool. It’s a great example of a practical instrument that a maker can build from scratch, with all design files provided to encourage modification and replication.

#### 8. Yertle: A 3D-Printed Quadruped for Locomotion Research
*   **What It Is:** A four-legged, 3D-printed walking robot designed as an open-source platform for studying locomotion.
*   **How It Works Technically:** The robot's mechanical structure is built from 3D-printed parts. The hardware is controlled by software written in C++ and Python. These languages are used to connect the physical robot to control algorithms, simulation environments, and machine-learning frameworks.
*   **Standout Details:**
    *   **Type:** Quadruped robot
    *   **Construction:** 3D-printed
    *   **Software Stack:** C++, Python
*   **Why Makers Care:** It’s an accessible platform for advanced robotics. Rather than a simple kit, it's a research tool that requires full engagement in assembly, electronics, programming, and calibration, making it a deep learning experience.

### **DIY Electronics**

#### 9. A CYD Project Menu for Makers
*   **What It Is:** Not a single project, but a curated directory of projects for the inexpensive ESP32-based "Cheap Yellow Display" (CYD).
*   **How It Works Technically:** This is a community-managed GitHub repository that acts as a central index. It provides links, flashing tools, and information for turning a CYD into various devices, such as a music dashboard, F1 notifier, game system, or 3D-printer panel.
*   **Standout Details:**
    *   **Hardware Platform:** ESP32 Cheap Yellow Display (CYD)
    *   **Content:** A curated list of diverse community projects and tools.
*   **Why Makers Care:** It's a valuable time-saving resource. It aggregates community knowledge for a popular, low-cost piece of hardware, showing its versatility and providing a jumping-off point for numerous projects.

### **IoT**

#### 10. Turning an E-Waste PC into a Router
*   **What It Is:** A project documenting the process and software challenges of converting an old PC into a network router.
*   **How It Works Technically:** The builder used an old Intel motherboard with 82574L network ports. An attempt to install OpenWrt failed because the OS was missing the `e1000e` driver module for the network hardware, rendering the ports invisible. The project then pivoted to successfully testing OPNsense as an alternative firewall/router platform.
*   **Standout Details:**
    *   **Hardware:** e-waste x86 PC with Intel 82574L network ports.
    *   **Software Issue:** OpenWrt lacked the required `e1000e` network driver.
    *   **Alternative Software:** OPNsense was evaluated.
*   **Why Makers Care:** This is a perfect "real-world troubleshooting" story. It underscores that hardware projects are often at the mercy of software and driver support, and it offers a practical comparison between different open-source router platforms.

### **Raspberry Pi**

#### 11. Run a Powerwall Grafana Dashboard on a Raspberry Pi
*   **What It Is:** A read-only dashboard that monitors and visualizes data from a Tesla Powerwall.
*   **How It Works Technically:** A Raspberry Pi runs software to collect battery, solar, household, and grid data directly from the Powerwall. This data is stored in a time-series database. Grafana is used to query the database and present the information in detailed historical graphs and dashboards. The system does not have control capabilities.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi
    *   **Software Stack:** Grafana, time-series database
    *   **Target:** Tesla Powerwall
*   **Why Makers Care:** It’s a safe, non-invasive way to gain deep insight into a complex home energy system. It uses industry-standard open-source tools (Grafana) on low-cost hardware to create a powerful, local data visualization tool.

#### 12. A Raspberry Pi Repeater Daemon in Python
*   **What It Is:** Software for creating a communications repeater using a Raspberry Pi.
*   **How It Works Technically:** A Python daemon, part of the OpenHop project, runs on a Raspberry Pi-class computer. This daemon acts as the controller that links communications software to external radio or audio hardware, turning the whole setup into a repeater.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi-class Linux computer
    *   **Software:** OpenHop repeater daemon
    *   **Language:** Python
    *   **Project Stats:** 1,274 commits, 277 stars
*   **Why Makers Care:** For anyone interested in amateur radio or audio projects, this provides the software core for a repeater. The high commit count suggests it's a mature and maintained project, although users will need to verify wiring and setup specifics.

#### 13. Build an Automated Raspberry Pi All-Sky Camera
*   **What It Is:** The software framework to run an unattended camera for capturing images of the entire night sky.
*   **How It Works Technically:** A Raspberry Pi runs software that uses the INDI (Instrument-Neutral-Distributed-Interface) protocol to communicate with and control compatible astronomy hardware (cameras, lenses). It automates the process of capturing image frames all night for later processing into time-lapses or composite images.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi
    *   **Protocol:** INDI
    *   **Scope:** This is the software foundation; the maker must provide the camera, lens, enclosure, power, and storage.
*   **Why Makers Care:** It automates a complex task for astrophotography. Using the INDI standard makes it compatible with a wide range of dedicated astronomy gear, moving beyond a simple Pi camera.

#### 14. Build a Raspberry Pi Homelab Monitor
*   **What It Is:** A self-hosted dashboard for monitoring the health of home lab computers and Docker containers.
*   **How It Works Technically:** The `homelab-monitor` software runs on a Raspberry Pi, providing a centralized web dashboard that displays host and container health metrics. It also includes an MCP server for compatible monitoring clients.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi
    *   **Function:** Local dashboard for host and Docker container health.
    *   **Feature:** Includes an MCP server.
*   **Why Makers Care:** It addresses a common pain point for anyone running multiple services at home: the lack of a single, unified monitoring view. It's a promising local alternative to cloud-based services, though details need to be verified from the repository.

### **Robotics**

#### 15. Inside Pistonudo: A Student-Built WRO Robot
*   **What It Is:** The complete project documentation from the ChaBots team for their Pistonudo robot, built for the WRO Future Engineers 2026 competition.
*   **How It Works Technically:** This repository is a detailed record of an entire robotics project. It covers the evolution of the robot's mechanics, electronics, and software for autonomous obstacle handling. Crucially, it also documents the team's process, including lessons learned from the previous season, testing strategies, serviceability design, and cost planning.
*   **Standout Details:**
    *   **Project:** Pistonudo robot for WRO Future Engineers 2026
    *   **Scope:** Documents the entire build process, including mechanics, electronics, software, testing, serviceability, and cost planning.
*   **Why Makers Care:** This is a "process-as-a-project." It offers a rare, detailed look into the entire lifecycle of a competition robot, providing invaluable insights not just on technical solutions but also on the project management and strategic planning required for success.