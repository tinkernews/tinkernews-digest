TO: Podcast Hosts
FROM: Research Editor
DATE: 2026-11-16
SUBJECT: Episode Brief for TinkerNews Issue #62

Here is the detailed brief for our upcoming episode covering TinkerNews Issue #62. Each project is broken down into what it is, its technical workings, standout details, and its relevance to our maker audience. All information is taken directly from the source material.

---

### **DIY Electronics**

**1. Build a $10-Class RISC-V Handheld Game Console**
*   **What It Is:** A handheld game console powered by a coin-cell battery, built around an extremely inexpensive RISC-V microcontroller.
*   **How It Works Technically:** The device is based on a custom PCB that integrates the microcontroller, a tiny monochrome screen, simple controls, and low-power audio components. The enclosure is 3D-printed. It can run several different firmware options.
*   **Standout Details:**
    *   **Chip:** CH32V003 (a RISC-V chip costing around ten cents).
    *   **Power:** Coin-cell battery.
    *   **Display:** Tiny monochrome screen.
    *   **Construction:** Custom PCB, 3D-printed case.
*   **Why a Maker Cares:** This project demonstrates extreme cost optimization in creating a complete, functional device. It's a case study in minimalist hardware design, low-power considerations for coin-cell operation, and understanding the practical limits (like battery life and programming hardware) of using ultra-cheap components.

**2. Making a Low-Power Bike Computer**
*   **What It Is:** A prototype bike computer designed for high power efficiency, fast response time, and outdoor screen readability.
*   **How It Works Technically:** The prototype uses an ESP32-S3 and prioritizes software efficiency over raw processing power. It minimizes power consumption by using techniques like damage-based rendering (only redrawing parts of the screen that change), simplified vector maps, cached map tiles, and careful memory management. The core strategy is to keep wake times as short as possible.
*   **Standout Details:**
    *   **Chip:** ESP32-S3.
    *   **Software Stack:** Uses damage-based rendering, simplified vector maps, tile caching, and specific memory management techniques.
*   **Why a Maker Cares:** It's a practical lesson in low-power design for battery-operated devices with displays. It shows that clever software optimization—focusing on efficient pixel updates and minimizing active time—can be more important for battery life than just choosing a fast processor.

**3. Give an Amstrad PCW Wi-Fi with PerryFi 2**
*   **What It Is:** A hardware add-on that provides Wi-Fi connectivity to a vintage Amstrad PCW computer through its original expansion interface.
*   **How It Works Technically:** It's a dual-microcontroller design. A Raspberry Pi Pico manages the hardware serial communication with the PCW. An ESP-12F module provides the Wi-Fi connection, exposing modem-style commands and handling the networking protocols (SLIP and PPP). Builders must flash separate firmware to each chip and use a specific boot disk image on the PCW.
*   **Standout Details:**
    *   **Chips:** Raspberry Pi Pico, ESP-12F.
    *   **Protocols:** Serial, SLIP (Serial Line Internet Protocol), PPP (Point-to-Point Protocol).
    *   **Interface:** Connects directly to the Amstrad PCW's expansion interface.
*   **Why a Maker Cares:** This is a classic retro-modern bridging project. It demonstrates how to combine two different, inexpensive microcontrollers to tackle a complex task: one for legacy hardware interfacing (Pico) and one for modern networking (ESP-12F). It's a great example of augmenting vintage computers with current technology.

---

### **3D Printing**

**1. Turning an Ender-3 into a PicoEMP Rig**
*   **What It Is:** A modification that turns a stock Ender-3 V3 SE 3D printer into a repeatable electromagnetic fault injection (EMFI) testing rig using a PicoEMP probe.
*   **How It Works Technically:** A custom 3D-printed mount holds the PicoEMP probe on the printer's tool head. Another printed part holds the target chip in an indexed position on the print bed. The printer's motion system is controlled via USB serial commands, with Python wrappers used to automate the process, turning manual probing into logged coordinate sweeps over a chip.
*   **Standout Details:**
    *   **Hardware:** Stock Ender-3 V3 SE, PicoEMP probe.
    *   **Software:** Python wrappers, USB serial control.
    *   **Function:** Automates EMFI testing by using G-code coordinates for precise probe positioning.
*   **Why a Maker Cares:** This shows how to repurpose a common and affordable tool (a 3D printer) into a specialized piece of hardware security test equipment. It highlights the value of a printer's precise motion control system for tasks beyond printing. The project also serves as a reminder of the importance of high-voltage safety and accounting for mechanical error in such setups.

**2. Bambu Bar Puts Printer Status in Your Menu Bar**
*   **What It Is:** A desktop utility for Mac and other systems that displays the status of Bambu Lab 3D printers in the system's menu bar or tray.
*   **How It Works Technically:** The application runs on a desktop computer and communicates with Bambu Lab printers over the local network. It reads data like print progress, temperatures (nozzle, bed), filament information, error states, and can display the printer's camera view. It can manage multiple printers and offers some limited control functions if the printer allows them.
*   **Standout Details:**
    *   **Protocol:** Local network communication (not cloud-based).
    *   **Features:** Monitors progress, temperatures, filament, errors, camera. Supports multiple printers.
    *   **Platform:** Desktop utility for menu bar/system tray.
*   **Why a Maker Cares:** It’s a useful tool for anyone with a Bambu printer who wants at-a-glance status updates without relying on a cloud service or a mobile app. It's a good example of a small, focused application that leverages a device's local network API for better user experience.

---

### **Arduino**

**1. Run BASIC Directly on an Arduino**
*   **What It Is:** A project called Tiny Basic that turns a mid-range Arduino into a self-contained computer running the BASIC programming language.
*   **How It Works Technically:** Tiny Basic includes an in-hardware editor, allowing users to write, edit, and run programs directly on the Arduino via a serial terminal, without needing to recompile and upload from a PC IDE for every code change. The library provides commands for hardware I/O (like reading pins), math, and bit manipulation.
*   **Standout Details:**
    *   **Software:** Tiny Basic interpreter and in-hardware editor.
    *   **Functionality:** Self-hosted programming environment on the microcontroller itself.
    *   **Features:** Includes hardware I/O commands.
*   **Why a Maker Cares:** This project brings back the interactive, immediate feel of early home computers. It allows for rapid, hands-on experimentation directly on the hardware, making it a great educational tool and a fun way to work on a project without the constant compile-upload cycle.

**2. Arduino scanner for 1991-95 Jeep computers**
*   **What It Is:** A low-cost diagnostic tool using an Arduino Nano to read data from the engine computers (ECUs) of 1991-95 Jeeps, which use a pre-OBD-II protocol.
*   **How It Works Technically:** An Arduino Nano is wired to the Jeep's diagnostic connector. It runs custom code to communicate using the proprietary SCI (Serial Communications Interface) protocol. A companion Python script on a laptop acts as the scanner interface, displaying fault codes and live data, recording drives, and running tests. The project requires careful wiring and voltage checks before connecting.
*   **Standout Details:**
    *   **Hardware:** Arduino Nano (costing around $3).
    *   **Vehicle:** 1991-95 Jeeps.
    *   **Protocol:** SCI (Serial Communications Interface).
    *   **Software Stack:** Arduino code for the SCI protocol, Python script for the user interface.
*   **Why a Maker Cares:** It's an excellent example of reverse-engineering and interfacing with proprietary, legacy automotive systems using cheap, off-the-shelf maker hardware. It empowers vehicle owners to perform diagnostics that would otherwise require rare and expensive professional tools.

**3. ExcaliPad: USB-C Keyboard and Game Controller**
*   **What It Is:** A single-PCB custom input device featuring tactile buttons and a two-axis thumb joystick.
*   **How It Works Technically:** The board is built around an ATmega32U4 microcontroller, which has native USB capabilities. This allows the board to be programmed to act as a standard USB HID (Human Interface Device), such as a keyboard, gamepad, or a custom device. Its firmware can be adapted for various uses.
*   **Standout Details:**
    *   **Chip:** ATmega32U4 (key for its native USB support).
    *   **Interface:** USB-C.
    *   **Inputs:** Tactile buttons, two-axis thumb joystick.
    *   **Functionality:** Can emulate a keyboard, gamepad, or custom HID device.
*   **Why a Maker Cares:** This is a highly versatile building block for creating custom computer interfaces. Because it's based on the ATmega32U4, it's compatible with the vast Arduino ecosystem. Makers can use it for gaming, creating macro pads, mouse controllers, accessibility tools, or application-specific control panels.

---

### **ESP32**

**1. This ESP32 Runs a Complete IBM PC/XT**
*   **What It Is:** A complete, functional IBM PC/XT compatible computer built on a single, postcard-sized board, powered by a single ESP32 chip.
*   **How It Works Technically:** The ESP32's dual-core architecture is key. One core is dedicated to generating the VGA video signal timing, while the other core handles the 8086 CPU emulation. The board includes physical VGA and PS/2 ports for a monitor and keyboard, a microSD card slot for storage (emulating a hard drive with DOS), and audio output.
*   **Standout Details:**
    *   **Chip:** ESP32.
    *   **Architecture:** Dual-core implementation splitting video generation and 8086 emulation.
    *   **I/O:** VGA output, PS/2 ports, microSD storage, audio.
    *   **Software:** Emulates an 8086 CPU and runs DOS.
*   **Why a Maker Cares:** This is a masterwork of retro-computing and real-time firmware development. It shows the sheer power of a modern, cheap microcontroller like the ESP32. It's a great project to study for anyone interested in emulation, real-time constraints (like VGA signal generation), and compact PCB design.

**2. ESP32 Arcade Matrix With HUB75 Panels**
*   **What It Is:** A system that uses an ESP32 to drive HUB75-type RGB LED matrix panels, turning them into a connected display for various arcade-themed or smart-home purposes.
*   **How It Works Technically:** An ESP32 controls the HUB75 panels directly. A MicroSD card is used to store settings and media files. The ESP32's Wi-Fi is used to connect to services like weather APIs, MQTT brokers, and Home Assistant to display real-time data. Using a more powerful ESP32-S3 allows for driving larger panels and more complex graphics.
*   **Standout Details:**
    *   **Chip:** ESP32 (ESP32-S3 recommended for larger displays).
    *   **Display:** HUB75 RGB matrix panels.
    *   **Storage:** MicroSD card.
    *   **Connectivity:** Wi-Fi.
    *   **Protocols/Services:** MQTT, Home Assistant integration.
*   **Why a Maker Cares:** This project provides a powerful, flexible firmware base for creating custom, Wi-Fi connected LED displays. It's perfect for building arcade marquees, information dashboards, or retro-style media players, and it integrates well with the smart home ecosystem.

**3. One ESP32 Firmware Base for Many E-Paper Displays**
*   **What It Is:** A unified ESP-IDF firmware designed to work with multiple different e-paper display families, simplifying development.
*   **How It Works Technically:** The firmware is built on a shared driver interface. Its operational loop is: wake from sleep, connect to Wi-Fi, fetch a pre-rendered image frame from a server (called Tesserae), refresh the e-paper screen, report its status, and go back to deep sleep. This architecture keeps board-specific support, provisioning, and power management code consolidated in one place.
*   **Standout Details:**
    *   **Framework:** ESP-IDF.
    *   **Architecture:** Shared driver interface for multiple display types.
    *   **Workflow:** Wake -> Wi-Fi connect -> Fetch frame -> Refresh screen -> Sleep.
    *   **System:** Designed to work with a server-side component (Tesserae) that provides the display content.
*   **Why a Maker Cares:** It solves a common problem: writing bespoke code for every different e-paper display. This project offers a standardized, reusable, and power-efficient firmware structure. Makers can adapt it for their own low-power display projects without reinventing the wheel for device provisioning, updates, and power management.

**4. ESP32 Gadgets Get Host-Controlled Dashboard Widgets**
*   **What It Is:** A software development kit (Hermes Gadget SDK) that allows a Linux host to push small, widget-like dashboard pages to an ESP32-based voice gadget.
*   **How It Works Technically:** The ESP32 gadget connects to a Linux host. The host can then publish widgets (displaying values, progress bars, lists, or headlines) to the gadget's screen, which appear alongside its normal idle clock. The system includes practical features like gesture support, fallback tiles if the connection is lost, expiration times for data, and handling for voice command interruptions.
*   **Standout Details:**
    *   **Platform:** Hermes Gadget SDK for ESP32 and a Linux host.
    *   **Functionality:** Pushes widgets from host to ESP32 device screen.
    *   **Features:** Supports various widget types (values, lists), gestures, fallback states, and expiration.
*   **Why a Maker Cares:** This provides a structured way to create sophisticated, interactive displays on peripheral smart devices. Instead of all logic living on the ESP32, the heavy lifting can be done on a more powerful host, with the ESP32 acting as a "thin client" display. This is a powerful architecture for building smart home status screens or companion displays.

---

### **IoT**

**1. Hands-On LoRa Link with Two Arduino Unos**
*   **What It Is:** A web-based browser simulation of a point-to-point LoRa communication link between two Arduino Unos equipped with SX1278 radio modules.
*   **How It Works Technically:** The simulation allows a user to inspect the virtual wiring, view the Arduino sketches for both the transmitter and receiver, and observe LoRa parameters in real-time. As the user moves the virtual radios apart, they can see changes in RSSI (Received Signal Strength Indicator) and packet airtime. It allows for testing what happens when settings (like spreading factor or frequency) are mismatched.
*   **Standout Details:**
    *   **Platform:** Browser-based simulation.
    *   **Hardware Simulated:** Arduino Uno (x2), SX1278 LoRa modules.
    *   **Data Displayed:** Arduino code, packet airtime, RSSI.
*   **Why a Maker Cares:** It's a zero-cost, no-hardware-required way to learn the fundamentals of LoRa communication. Beginners can understand how LoRa works, see the code, and experiment with parameters to see their effects on range and reliability before ever buying physical modules.

**2. Building a Solar LoRaWAN Sensor Node**
*   **What It Is:** A solar-powered, long-range wireless sensor node for agricultural monitoring, named the Green Dot Board.
*   **How It Works Technically:** The board is built around an RP2040 microcontroller and a LoRa-E5 module for LoRaWAN connectivity. It manages power from both a solar panel and a LiPo battery. The firmware, written in MicroPython, reads temperature and humidity sensors, packs the data efficiently, and transmits it via the LoRa-E5 module to a Loriot dashboard. The board also includes an RS485 interface for connecting sensors over longer wired distances.
*   **Standout Details:**
    *   **Chips:** RP2040, LoRa-E5 module.
    *   **Power:** Solar and LiPo.
    *   **Software:** MicroPython.
    *   **Protocols:** LoRaWAN, RS485.
    *   **Sensors:** Temperature and humidity.
*   **Why a Maker Cares:** This is a complete blueprint for a self-sufficient, off-grid IoT sensor node. It combines power management, a popular microcontroller (RP2040), long-range communication (LoRaWAN), and industry-standard sensor interfacing (RS485) in a single project.

**3. Build a Local ESP32 Gateway for Wallbox Control**
*   **What It Is:** A gateway device, built with a ~$15 ESP32 board, that allows local network control of a Wallbox Pulsar EV charger, bypassing the company's cloud servers.
*   **How It Works Technically:** The ESP32 connects to the Wallbox charger via Bluetooth Low Energy (BLE). It then connects to the local Wi-Fi network and acts as a bridge, exposing control via MQTT and integrating with Home Assistant. It can record charging sessions, hosts its own local web dashboard, and supports over-the-air (OTA) firmware updates.
*   **Standout Details:**
    *   **Hardware:** ESP32 board.
    *   **Connectivity:** BLE (to charger), Wi-Fi (to local network).
    *   **Protocols:** MQTT, BLE.
    *   **Features:** Home Assistant integration, local dashboard, OTA updates.
*   **Why a Maker Cares:** This project is a prime example of "de-clouding" a commercial smart device. It gives the user full local control, ensuring the device works even if the manufacturer's servers go down or the internet is out. It's a great project for privacy, reliability, and custom automation.

**4. Smart Home Devices That Work Offline**
*   **What It Is:** A design philosophy and technical approach for building smart home devices that prioritize local network operation and do not depend on the internet for core functionality.
*   **How It Works Technically:** The proposed design uses ESP8266 or ESP32 microcontrollers running Tasmota firmware. Devices communicate on the local network using the MQTT protocol. A local automation server (like Home Assistant) handles the logic. Internet access is only used for optional features like remote control when away from home or notifications, but the primary functions (like turning on a light switch) work entirely offline.
*   **Standout Details:**
    *   **Hardware:** ESP8266, ESP32.
    *   **Software:** Tasmota firmware.
    *   **Protocol:** MQTT.
    *   **Architecture:** "Local-first" design, where core functions do not require cloud access.
*   **Why a Maker Cares:** This addresses a major pain point with commercial smart home products: dependency on external servers. It provides a robust, reliable, and privacy-respecting blueprint for DIY smart home devices. It’s less a single project and more a fundamental design pattern for building a better smart home.

---

### **Raspberry Pi**

**1. TelltaleDNS: A Raspberry Pi DNS Server With Per-Device Rules**
*   **What It Is:** A DNS server, written in Rust, that can run on a Raspberry Pi to intercept, log, and filter DNS requests from all devices on a home network.
*   **How It Works Technically:** TelltaleDNS is set up as the primary DNS server for the network. It receives all DNS queries, logs them, and applies custom rules based on the device or group of devices making the request. It can explain why a request was blocked or allowed, and forwards permitted requests to an upstream DNS server of the user's choice.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi.
    *   **Software:** Written in Rust.
    *   **Functionality:** Logs queries, applies per-device filtering rules.
*   **Why a Maker Cares:** This gives a maker granular control and visibility over their home network traffic. It’s a powerful tool for ad-blocking, parental controls, or blocking telemetry from IoT devices, all from a central, self-hosted point.

**2. RS-Key: A Raspberry Pi Security Key**
*   **What It Is:** A project that turns a Raspberry Pi RP2350 into a multi-protocol hardware security key.
*   **How It Works Technically:** The device runs custom firmware written in Rust. It can handle several security protocols, enabling it to function as a key for passkeys (FIDO2/WebAuthn), SSH, Git commit signing, smart-card applications, and generating one-time passwords. A version with a touchscreen keeps the PIN entry and approval actions physically on the device for higher security.
*   **Standout Details:**
    *   **Chip:** Raspberry Pi RP2350.
    *   **Software:** Firmware written in Rust.
    *   **Protocols:** Supports passkeys, SSH, Git signing, smart-card, OTP.
    *   **Features:** Touchscreen version for on-device PIN entry and approval.
*   **Why a Maker Cares:** This is a DIY, open-source alternative to commercial security keys like a YubiKey. It's a deep dive into modern digital security protocols and an excellent showcase for the capabilities of the new RP2350 chip. Makers can build their own key and have full transparency into its operation.

**3. Pico 2 W Recovery for the M-VAVE FM-1**
*   **What It Is:** A recovery method for the M-VAVE FM-1 audio device using a Raspberry Pi Pico 2 W to safely access its mask-ROM bootloader.
*   **How It Works Technically:** The Pico 2 W is used as a programmer to interface with the FM-1. The recovery process involves comparing firmware dumps from a fresh device, carefully limiting writes to only the application area of the memory (to avoid bricking), and reading back sectors to verify the write was successful.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi Pico 2 W, M-VAVE FM-1.
    *   **Function:** Provides a controlled method to enter the mask-ROM bootloader for firmware recovery or modification.
*   **Why a Maker Cares:** This is a hardware hacking and reverse engineering project. It demonstrates a safe procedure for flashing firmware onto a device that might otherwise be difficult to recover, a common challenge when modifying consumer electronics.

---

### **Robotics**

**1. Four-Servo Arm Control in a Browser**
*   **What It Is:** A browser-based simulation of a simple four-servo robotic arm controlled by an Arduino Uno and two thumb joysticks.
*   **How It Works Technically:** The simulation models the hardware setup and provides a testbed for developing the control code. It demonstrates concepts like rate-based joint control (moving the servo at a certain speed rather than to a fixed position), setting angle limits, handling joystick dead-bands, and processing serial feedback from the Arduino.
*   **Standout Details:**
    *   **Platform:** Browser-based simulation.
    *   **Hardware Simulated:** Arduino Uno, SG90 servos (x4), thumb joysticks (x2).
    *   **Concepts:** Rate-based control, angle limits, dead-band handling.
*   **Why a Maker Cares:** Like the LoRa simulator, this is a fantastic learning tool. It allows makers to develop and debug the logic for controlling a robot arm in a safe, virtual environment before dealing with the complexities of real-world physics, power requirements, collisions, and servo limitations.

**2. A Simulated MeArm Robot Plays Connect Four**
*   **What It Is:** A simulation where a virtual MeArm robot plays the game Connect Four against a human player.
*   **How It Works Technically:** The simulation uses the PyBullet physics engine to handle gravity, collisions, and the arm's movement. The control code, written in Python, separates the game's display window from the physics process. The robot's moves are chosen using a Minimax algorithm. The simulation requires careful calibration data and pre-defined safe movement steps to prevent the virtual arm from colliding with the game board.
*   **Standout Details:**
    *   **Software:** Python, PyBullet (physics engine), Minimax (game AI).
    *   **Robot:** Simulated MeArm.
    *   **Concepts:** Physics simulation, game theory AI, robot path planning.
*   **Why a Maker Cares:** This project connects robotics with AI and physics simulation. It’s a great introduction to using professional-grade tools like PyBullet and classic AI algorithms (Minimax) to create autonomous robotic behavior, all within a sandboxed virtual environment.

**3. A Webcam-Guided MeArm Sorts Colored Balls**
*   **What It Is:** A physical, 3D-printed MeArm robot that uses a webcam to find and sort colored balls.
*   **How It Works Technically:** A standard webcam is used for vision. A Python script processes the camera feed to identify the colored balls and calculate their positions in millimeters. This coordinate data is then sent to an Arduino, which controls the four SG90 servos of the MeArm to execute a calibrated pick-and-place sequence. The design uses fixed motion limits in the software to make the inexpensive hardware operate more reliably.
*   **Standout Details:**
    *   **Hardware:** Printed MeArm, Arduino, SG90 servos (x4), webcam.
    *   **Software Stack:** Python for computer vision and high-level control, Arduino for low-level servo movement.
*   **Why a Maker Cares:** This is a classic "pick and place" computer vision project that is very accessible. It demonstrates a common robotics architecture where a PC handles complex tasks (vision) and a microcontroller handles real-time hardware control. It also shows how software constraints can improve the reliability of cheap hardware.

**4. How This Robot Finds and Collects Trash**
*   **What It Is:** A mobile robot, built on a Traxxas RC car chassis, that can autonomously identify, approach, and pick up trash.
*   **How It Works Technically:** The robot uses a multi-sensor approach. An OAK-D Lite camera is used for object detection (spotting the trash). An LD19 LiDAR sensor is used for distance measurement, allowing the robot to accurately stop a specific distance away from the target (0.16 meters). A Raspberry Pi 5 acts as the main brain, taking the data from these sensors and issuing simple control commands to the chassis and an SO101 robotic arm for the final pickup.
*   **Standout Details:**
    *   **Chassis:** Traxxas base.
    *   **Controller:** Raspberry Pi 5.
    *   **Sensors:** OAK-D Lite (for vision/detection), LD19 LiDAR (for distance).
    *   **Actuator:** SO101 arm.
*   **Why a Maker Cares:** This is a sophisticated real-world robotics project that demonstrates sensor fusion. By using one sensor for *what* an object is (OAK-D) and another for *where* it is (LiDAR), the complex control task is simplified for the Raspberry Pi. It’s a great example of a robust system architecture for autonomous mobile robots.