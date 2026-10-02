**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-09-08
**SUBJECT:** Episode Brief: TinkerNews Issue #37

Here is the detailed brief for our upcoming episode covering TinkerNews #37. I've broken down every project according to the source material, focusing on the technical details and the "why it matters" for our maker audience.

---

### **Episode Brief: TinkerNews #37 - Build Smarter, Repair Deeper**

#### **3D PRINTING**

**1. Converting a K1 SE Toward K1C Features**
*   **What It Is:** A documented community discussion on upgrading a Creality K1 SE 3D printer to include cooling and temperature sensing features found on the K1C model.
*   **How It Works Technically:** This is a hardware and software modification. It requires physically adding new fans and a thermistor, along with the associated wiring. On the software side, the printer's firmware must be modified and the Klipper configuration updated to recognize and use the new hardware. The source warns that simply flashing K1C firmware onto a K1 SE is not a safe or viable approach.
*   **Standout Details:**
    *   **Hardware:** Fans, thermistor, wiring.
    *   **Software:** Firmware modification, Klipper configuration.
*   **Why a Maker Cares:** This project goes beyond simple 3D-printed upgrades. It's a case study in deep-level hardware modification that requires interacting with the machine's firmware and core configuration, demonstrating how to add significant functionality to existing maker tools.

---

#### **ARDUINO**

**1. Add 16 I/O Pins with a PCF8575**
*   **What It Is:** A tutorial for using a PCF8575 module to add 16 digital I/O pins to a microcontroller.
*   **How It Works Technically:** The PCF8575 module communicates with a host board (like an Arduino, ESP8266, or ESP32) over the I2C protocol, using only the SDA and SCL pins. A provided software library handles the low-level I2C communication, making the extra pins easy to use. The build uses LEDs and buttons for a hands-on test.
*   **Standout Details:**
    *   **Chip:** PCF8575.
    *   **Added I/O:** 16 digital lines.
    *   **Protocol:** I2C.
    *   **Host Boards:** Arduino, ESP8266, ESP32.
*   **Why a Maker Cares:** This is a fundamental solution to a common problem: running out of GPIO pins on a project. It shows how to expand a board's capabilities with a cheap, widely available module and a simple two-wire interface, keeping the board’s native pins free for other tasks.

**2. Build an Arduino/ESP32 OBD2 K-Line Tool**
*   **What It Is:** A software library that allows an Arduino or ESP32 to communicate with the engine control units (ECUs) of older cars that use the K-Line diagnostic protocol.
*   **How It Works Technically:** The library implements the K-Line protocol's timing and commands in software. To work, a maker must build a circuit with a "proper protected transceiver" to safely interface the microcontroller's logic levels with the vehicle's electrical system. The library's examples and source code are crucial for verifying supported protocols and wiring before connecting to a car.
*   **Standout Details:**
    *   **Protocol:** K-Line (distinct from modern CAN bus).
    *   **Host Boards:** Arduino, ESP32.
    *   **Hardware Prerequisite:** Requires a protected transceiver hardware interface.
*   **Why a Maker Cares:** This project opens up the world of automotive diagnostics for older vehicles that modern OBD2 scanners may not support. It's a practical entry point for makers interested in reverse-engineering or logging data from pre-CAN bus cars.

**3. BoatOpenIO v2: Modular Marine Gateway Main Board**
*   **What It Is:** The main circuit board for a modular boat gateway system designed for signal routing and impact detection.
*   **How It Works Technically:** The board uses a 16:1 multiplexer to channel various analog inputs into a single ADS1115 analog-to-digital converter. An onboard MPU6050 is used for impact sensing. The design emphasizes repairability with socketed parts and swappable modules. This board is just one piece of a four-board system and requires companion hardware to function.
*   **Standout Details:**
    *   **Chips:** ADS1115 (ADC), MPU6050 (IMU).
    *   **Components:** 16:1 multiplexer, socketed parts.
*   **Why a Maker Cares:** This is a good example of modular and repair-friendly PCB design for a harsh environment. The use of a multiplexer to save on ADC inputs is a classic, cost-effective design pattern.

---

#### **DIY ELECTRONICS**

**1. ESP32 Hot-Air SMD Rework Station**
*   **What It Is:** A DIY hot-air station for surface-mount device (SMD) rework, controlled by an ESP32.
*   **How It Works Technically:** The system uses a thermocouple to measure the air temperature, providing feedback to the ESP32. The ESP32 runs MicroPython firmware that implements a PID control loop to precisely regulate the heater. Airflow is also programmable. The project is a full system build with a custom PCB and requires careful attention to high-temperature insulation, grounding, and power management.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **Firmware:** MicroPython.
    *   **Control:** PID control loop.
    *   **Sensor:** Thermocouple.
    *   **Design:** Custom PCB.
*   **Why a Maker Cares:** It's a sophisticated tool-build that goes far beyond assembling pre-made modules. Makers get a powerful, programmable rework station while learning about PID control, high-temperature sensing, and power electronics safety—skills directly applicable to building other controlled tools.

**2. Reverse-Engineering a Failed Fellow Opus Grinder**
*   **What It Is:** A teardown and failure analysis of a 2023 Fellow Opus coffee grinder, comparing it to a 2025 replacement model.
*   **How It Works Technically:** The grinder failed due to two snapped capacitor legs. The teardown revealed its construction: a layered Class II enclosure with modular power and control boards. The simple design made diagnosis straightforward. The comparison between the two model years highlighted design changes relevant to appliance repair.
*   **Standout Details:**
    *   **Failure Point:** Snapped capacitor legs.
    *   **Construction:** Class II enclosure, modular power/control boards.
    *   **Years Compared:** 2023 vs. 2025 models.
*   **Why a Maker Cares:** This is a masterclass in practical reverse-engineering for repair. It shows how to approach a failed consumer appliance methodically, identify weak points, and learn valuable lessons about product design and evolution that can inform a maker's own projects.

**3. Reconstructing a Forgotten Microprofessor Sound Board**
*   **What It Is:** A project to digitally reconstruct the schematic and software for an obscure sound board for the Microprofessor computer system.
*   **How It Works Technically:** The reconstruction was done without the original hardware. The creator used historical photographs to understand the layout, a MAME ROM dump for the software, and their knowledge of the AY-3-8910 sound chip to piece together the design. The final output is a KiCad schematic and annotated software, not a physical replica. Some functions remain unverified due to missing manuals.
*   **Standout Details:**
    *   **Core Chip:** AY-3-8910.
    *   **Source Materials:** Photographs, MAME ROM dump.
    *   **Output:** KiCad schematic, annotated software.
*   **Why a Maker Cares:** This is digital archeology. It demonstrates how to preserve and understand vintage hardware even when physical examples are gone, using emulation tools, datasheets, and fragmentary evidence. It’s a great example of hardware preservation skills.

**4. OOMWOO: A Local, Open Robot Vacuum**
*   **What It Is:** An open-source, fully maker-built robot vacuum designed to run without cloud services.
*   **How It Works Technically:** This is a complete robotics system. A Raspberry Pi handles high-level processing, while microcontrollers manage motors and sensors. Navigation is done via LiDAR. The chassis is made of 3D-printed parts. The software stack is built on ROS2 and integrates with Home Assistant for local control.
*   **Standout Details:**
    *   **Computing:** Raspberry Pi and microcontrollers.
    *   **Sensor:** LiDAR.
    *   **Software:** ROS2, Home Assistant integration.
    *   **Key Feature:** No required cloud services.
    *   **Project Status:** Early development; full build instructions planned for Fall 2026.
*   **Why a Maker Cares:** For the ambitious maker, this is a chance to build a complex, modern robot from scratch. It touches on 3D printing, embedded systems, Linux, and robotics software (ROS2), all while championing the principles of local control and privacy.

---

#### **ESP32**

**1. ESP32-S3 Retrofit for Safer OpenTherm Control**
*   **What It Is:** A guide on upgrading a PIC-based NodoShop OpenTherm Gateway with an ESP32-S3 to add modern network capabilities.
*   **How It Works Technically:** The guide details replacing the original PIC microcontroller with a LOLIN S3 Mini. This adds Wi-Fi connectivity, allowing the gateway to be controlled via HTTP, REST, MQTT, and a web browser. The process emphasizes a safe rollout: flash the firmware, verify data locally on the network, and only then configure optional remote access.
*   **Standout Details:**
    *   **MCU:** ESP32-S3 (specifically a LOLIN S3 Mini).
    *   **Protocols Added:** Wi-Fi, HTTP, REST, MQTT.
    *   **Device Upgraded:** NodoShop OpenTherm Gateway.
*   **Why a Maker Cares:** This is a perfect example of a "smart" retrofit. It shows how to take an existing, functional piece of specialized hardware and add powerful IoT capabilities using a modern, inexpensive microcontroller, with a strong emphasis on security and staged testing.

---

#### **IoT**

**1. Build a Pocket BLE Privacy Scanner with an M5Stack**
*   **What It Is:** A portable tool, named GhostBLE, built with an M5Stack to scan for and display information from nearby Bluetooth Low Energy (BLE) advertisements.
*   **How It Works Technically:** The M5Stack's built-in BLE radio actively scans for advertising packets, which devices broadcast before pairing. The software parses these packets to show device names and other details on the M5Stack's display, flagging potential privacy concerns.
*   **Standout Details:**
    *   **Hardware:** M5Stack.
    *   **Protocol:** Bluetooth Low Energy (BLE) advertisements.
*   **Why a Maker Cares:** This project makes an abstract privacy concept tangible. It gives makers a practical tool to audit their own smart homes, labs, and BLE projects to see exactly what information their devices are broadcasting to the world, turning their maker skills toward digital self-defense.

**2. ELRO Hubs Send Real-Time Events to Home Assistant**
*   **What It Is:** A custom Home Assistant integration that pulls real-time data directly from ELRO Connects K1 and K2 security hubs.
*   **How It Works Technically:** The integration communicates directly with the ELRO hubs on the local network to read events, battery levels, signal strength, and device states. This allows for immediate local automations based on alarm or sensor triggers. The K1 and K2 hubs use different communication software, so the integration needs to identify the hardware version correctly.
*   **Standout Details:**
    *   **Platform:** Home Assistant.
    *   **Hardware:** ELRO Connects K1 and K2 hubs.
    *   **Data:** Real-time events, battery levels, signal strength.
*   **Why a Maker Cares:** It shows how to break a commercial, closed-ecosystem product out of its silo. By reading the hub directly, makers can integrate proprietary security sensors into their open, local smart home system for more powerful and customized automations.

**3. Bring TP-Link and Mercusys Routers into Home Assistant**
*   **What It Is:** A custom Home Assistant component that integrates data and controls from supported TP-Link and Mercusys routers.
*   **How It Works Technically:** The component is installed via the Home Assistant Community Store (HACS). It polls the router approximately every 30 seconds to gather status information. It adds new sensors and controls to Home Assistant. The source notes that router firmware updates can break compatibility and the integration might log out the admin user from the router's web interface while it's active.
*   **Standout Details:**
    *   **Platform:** Home Assistant (via HACS).
    *   **Hardware:** Supported TP-Link and Mercusys routers.
    *   **Update Rate:** Polling every ~30 seconds.
*   **Why a Maker Cares:** This integrates a core piece of network infrastructure into the smart home dashboard. Makers can create automations based on network status, connected devices, or other router data, providing a more holistic view and control over their home environment.

**4. How a $20 ESP8266 Calls and Tracks Elevators**
*   **What It Is:** A system that uses an ESP8266 to call an apartment elevator and track its position locally, without modifying the elevator's control system.
*   **How It Works Technically:** An ESP8266 is connected to a relay, which is wired in parallel with the existing hallway call button to simulate a press. An external camera with a permitted view is used to visually track the elevator's floor. The ESP8266 sends this information via MQTT to Home Assistant, which can show the status on a door-side display.
*   **Standout Details:**
    *   **MCU:** ESP8266.
    *   **Cost:** Approx. $20.
    *   **Actuation:** A relay to "press" the button.
    *   **Sensing:** A camera provides a video feed for tracking.
    *   **Protocol:** MQTT.
    *   **Integration:** Home Assistant.
*   **Why a Maker Cares:** This is a brilliant example of "black box" automation. It solves a real-world problem by interfacing with a system from the outside—observing and acting on it—without tampering with critical, off-limits infrastructure. It's creative, non-invasive problem-solving.

**5. A Self-Hosted UniFi Network Companion**
*   **What It Is:** A self-hosted application called Network Optimizer for troubleshooting UniFi networks.
*   **How It Works Technically:** The application can be run via Docker or on Windows. It connects to a UniFi controller to collect readings and access configuration data. The source strongly advises that users carefully review the repository and understand what controller access it requires and what data it collects before deploying it on a live network.
*   **Standout Details:**
    *   **Deployment:** Self-hosted (Docker, Windows).
    *   **System:** For UniFi networks.
*   **Why a Maker Cares:** For makers running more complex UniFi networks, this offers a potential alternative dashboard for troubleshooting. The project serves as a reminder of the security implications of giving third-party software access to network controller credentials.

**6. Anthbot Mowers in Home Assistant—An Unmaintained Integration**
*   **What It Is:** A community-built Home Assistant integration for Anthbot Genie 600, M5, and M9 robotic mowers, which is no longer maintained.
*   **How It Works Technically:** The integration works by looking up the user's account, making AWS IoT shadow requests to get the mower's status, and creating sensors in Home Assistant based on the mower's model. The source states it is unmaintained and suggests it should be used primarily as a technical reference, pointing users to a more current fork (`ha-anthbot-map-v2`).
*   **Standout Details:**
    *   **Platform:** Home Assistant.
    *   **Hardware:** Anthbot Genie 600, M5, M9 mowers.
    *   **Cloud Service:** AWS IoT.
    *   **Status:** Unmaintained.
*   **Why a Maker Cares:** This is a look into the lifecycle of open-source projects. It provides a valuable technical roadmap for how to interface with a cloud-dependent IoT device (via AWS IoT), even if the project itself is outdated. It’s a good starting point for someone wanting to revive the project or build a similar integration.

---

#### **RASPBERRY PI**

**1. USB SSD Boot or PXE Network Boot?**
*   **What It Is:** A comparison of alternatives to SD cards for booting a Raspberry Pi to improve reliability.
*   **How It Works Technically:**
    *   **USB SSD:** The simplest replacement; the Pi boots from an SSD connected via USB. NVMe is mentioned as a faster option for the Pi 5.
    *   **PXE Boot:** (Preboot Execution Environment) A more complex setup where multiple Pis boot over a wired network from a single server. This requires a dependable network and more initial configuration.
*   **Standout Details:**
    *   **Alternatives to SD Card:** USB SSD, NVMe (for Pi 5), PXE network boot.
*   **Why a Maker Cares:** SD card failure is a major pain point for any maker running a long-term Raspberry Pi project. This article directly addresses that problem, laying out the pros and cons of the most common, more reliable solutions.

**2. Build a Portable Offline Internet with a Raspberry Pi**
*   **What It Is:** A project that turns a Raspberry Pi into a self-contained, portable information server for use in areas without internet access.
*   **How It Works Technically:** The Raspberry Pi hosts its own private network connection. It runs services that provide local maps, a copy of Wikipedia, and local AI tools. The project highlights the practical trade-offs involved, such as storage capacity for the data, battery life for portability, and the Pi's processing speed limitations.
*   **Standout Details:**
    *   **Hosted Services:** Local maps, Wikipedia copy, AI tools.
    *   **Key Feature:** Operates fully offline over a private connection.
*   **Why a Maker Cares:** This is a compelling "information survival kit" project. It shows how a Pi can be used for data sovereignty and resilience, creating a valuable resource that doesn't depend on external infrastructure. It’s a great project for learning about self-hosting and resource management on a small computer.

**3. Build a Raspberry Pi Modbus Logger with Ansible**
*   **What It Is:** A system named LibrePiLogger for creating remote environmental data loggers using Raspberry Pis.
*   **How It Works Technically:** Raspberry Pis (either a Zero or a Pi 4) are connected to Modbus sensors via an RS-485 interface. The software records timestamped data into CSV files. The entire setup and configuration process is managed using Ansible, making it scalable. The system is designed to be extensible, allowing new sensor drivers to be added without a full rewrite.
*   **Standout Details:**
    *   **MCU:** Raspberry Pi (Zero or 4).
    *   **Protocol:** Modbus over RS-485.
    *   **Data Format:** Timestamped CSV files.
    *   **Configuration:** Ansible.
*   **Why a Maker Cares:** This project combines industrial-grade protocols (Modbus, RS-485) with modern DevOps tools (Ansible) on a maker platform (Raspberry Pi). It provides a robust, scalable, and professional framework for anyone needing to build reliable, multi-node sensor networks.

---

#### **ROBOTICS**

**1. Building Nexara: An Air-Gapped AI Avatar Head**
*   **What It Is:** A physical, animatronic head that serves as an interface for a local, air-gapped AI system.
*   **How It Works Technically:** The head has two round displays for eyes and a spatial camera for input. It moves on a three-axis servo-driven neck. An ESP32-S3 connects these components. The design uses separated power rails to isolate the sensitive electronics from the noisy servos. The entire system is proposed to be independent of cloud services.
*   **Standout Details:**
    *   **MCU:** ESP32-S3.
    *   **Hardware:** Dual round displays, spatial camera, three-axis servo neck.
    *   **Power Design:** Separated power rails for sensitive vs. noisy components.
    *   **Key Feature:** Designed to be air-gapped and not rely on cloud services.
*   **Why a Maker Cares:** This project brings an abstract concept—an AI—into the physical world. It's a great example of mechatronics, embedded systems, and practical electronic design (like isolating power rails for servos), all in the service of creating a more tangible, private AI interface.