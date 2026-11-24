**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-11-24
**SUBJECT:** Episode Brief: TinkerNews Issue #63

Here is the detailed research brief for this week's projects. All information is sourced directly from the newsletter.

---

### **Arduino**

**1. CornerSense Maps Motion Around a Blind Corner**

*   **What it is:** A tabletop prototype for a blind corner warning system.
*   **How it works technically:** Paired infrared checkpoints detect an object. An Arduino processes the sensor data to estimate the object's speed and arrival time, triggering local alerts. A Raspberry Pi is connected to provide a web dashboard and logs data to the ThingSpeak cloud service.
*   **Standout Details:**
    *   **Chips:** Arduino, Raspberry Pi.
    *   **Sensors:** Paired infrared checkpoints.
    *   **Software Stack:** Arduino sketch for sensing, Raspberry Pi for dashboard, ThingSpeak for logging.
*   **Why a Maker Cares:** This is a practical example of a dual-microcontroller system where each board handles a specific task: the Arduino for real-time sensing and the Pi for higher-level data processing, visualization, and cloud connectivity.

**2. Arduino SH1106 OLED Interface Over I2C**

*   **What it is:** A guide for connecting and programming a 1.3-inch SH1106 OLED display with an Arduino Uno or Nano.
*   **How it works technically:** The display connects to the Arduino via a four-wire I2C interface. The project guide explains how to use the correct library, scan for the I2C address, and use buffered drawing to display live counters, shapes, icons, and bitmaps. It also addresses common memory limitations and troubleshooting a blank screen.
*   **Standout Details:**
    *   **Chips:** Arduino Uno/Nano, SH1106 display driver.
    *   **Display:** 1.3-inch OLED.
    *   **Protocol:** I2C (4-wire).
    *   **Software Concepts:** Buffered drawing, I2C address scanning, bitmap display.
*   **Why a Maker Cares:** This is a fundamental tutorial for adding a small, crisp display to a project. It covers not just the "how" but also the common "why it's not working" problems, which is invaluable for beginners.

**3. Arduino SSD1306 OLED: Wiring to Animation**

*   **What it is:** A guide for using the popular 128x64 SSD1306 OLED display with an Arduino.
*   **How it works technically:** A four-wire I2C connection links the display to the Arduino. The tutorial uses the Adafruit library for setup and control. It demonstrates buffered drawing techniques to show everything from a first message to sensor readings, logos, and simple animations.
*   **Standout Details:**
    *   **Chips:** Arduino, SSD1306 display driver.
    *   **Display:** 128x64 OLED.
    *   **Protocol:** I2C (4-wire).
    *   **Software Stack:** Adafruit library, covers bitmap storage in memory.
*   **Why a Maker Cares:** The SSD1306 is one of the most common OLEDs in the hobbyist world. This project provides a complete walkthrough from basic wiring to creating a functional small device interface, making it a key skill for many embedded projects.

**4. Run Laya Decisions on the Arduino UNO Q**

*   **What it is:** A project that runs a local AI decision model named "Laya" on an Arduino UNO Q.
*   **How it works technically:** A Python application runs the Laya model using CPU-only PyTorch. This setup routes requests to the Arduino to make decisions like choosing a fixed option, checking if something is broken, or scoring urgency. The system can reject answers it is uncertain about before an action is triggered.
*   **Standout Details:**
    *   **Board:** Arduino UNO Q.
    *   **Software Stack:** Python, CPU-only PyTorch.
    *   **Technical Specs:** Manages a 322 MB model within 4 GB of RAM.
*   **Why a Maker Cares:** It demonstrates how to run a moderately sized AI model on relatively constrained, non-GPU hardware. The feature that rejects uncertain answers is a practical approach to building more reliable physical AI systems.

### **3D Printing**

**5. Snapmaker U1 Toolhead Swaps in 30 Seconds**

*   **What it is:** A firmware modification for the Snapmaker U1 3D printer that simplifies swapping toolheads.
*   **How it works technically:** This firmware fork stores calibration data (nozzle, flow, PID, offset) with the physical toolhead itself, not the slot it's plugged into. It uses USB serial detection to identify which toolhead is connected and offers a guided swap process.
*   **Standout Details:**
    *   **Hardware:** Snapmaker U1, requires specific supported USB-C cables and printed strain relief parts.
    *   **Software:** A custom firmware fork.
    *   **Process:** Uses USB serial detection and selective calibration.
*   **Why a Maker Cares:** For owners of multi-tool 3D printers, this solves a major workflow annoyance. It makes the machine smarter by associating settings with the physical hardware, reducing the need for constant recalibration.

### **DIY Electronics**

**6. Portable Fuzzy Logic on Embedded Boards**

*   **What it is:** A project demonstrating a portable fuzzy logic inference engine that can be moved between different embedded boards.
*   **How it works technically:** The fuzzy model is stored in a file, while a single inference engine, generated by MATLAB, is deployed to various microcontrollers. This approach is shown working on STM32, SAM3X8E, Raspberry Pi, and ESP32 boards.
*   **Standout Details:**
    *   **Chips:** STM32, SAM3X8E, Raspberry Pi, ESP32.
    *   **Software Stack:** MATLAB-generated C-code for the inference engine.
    *   **Concepts:** Requires work on memory management, file parsing, storage, and validation for embedded deployment.
*   **Why a Maker Cares:** This shows a powerful "write once, run anywhere" approach for complex logic. Instead of re-coding rules for each platform, you can reuse the same core engine, which is a big deal for portability and maintenance.

**7. A 16-LED Heart on a Rechargeable Nano**

*   **What it is:** A keychain-sized, portable LED heart built on a perfboard with an Arduino Nano.
*   **How it works technically:** An Arduino Nano controls 16 LEDs arranged in a heart shape, cycling through nine different patterns. The power system is self-contained, using a LiPo battery, a TP4056 charger with protection, an MT3608 boost converter for voltage, and battery sensing circuitry.
*   **Standout Details:**
    *   **Chips:** Arduino Nano, TP4056 (charger), MT3608 (converter).
    *   **Part Count:** 16 LEDs.
    *   **Power:** LiPo battery, 5V operation via boost converter.
    *   **Construction:** 50 × 70 mm perfboard.
*   **Why a Maker Cares:** This is a great small-scale project that forces a maker to deal with a complete embedded system: microcontroller, power regulation, charging, and user output, all in a compact, portable form factor.

**8. A Wi-Fi Archive for Camera Floppy Disks**

*   **What it is:** "floppy3.5" is a battery-powered Wi-Fi reader that accesses old 3.5-inch camera floppy disks and serves the photos over a local network.
*   **How it works technically:** The device uses two microcontrollers. An RP2354A is dedicated to controlling the 3.5-inch floppy drive and reading the FAT12 filesystem. An ESP32-S3 acts as a web server, hosting a local website at `floppy.local`. Photos are read from the floppy and stored on a microSD card to handle cases where cameras reuse filenames.
*   **Standout Details:**
    *   **Chips:** RP2354A, ESP32-S3.
    *   **Protocols:** Wi-Fi for web server, FAT12 for floppy disk.
    *   **Storage:** 3.5-inch floppy drive, microSD card.
*   **Why a Maker Cares:** This is a fantastic retro-tech project that combines low-level hardware control (floppy drive) with modern networking (Wi-Fi web server). The dual-MCU architecture is a smart way to divide complex tasks.

### **ESP32**

**9. An Offline ESP32-S3 Learning Lab**

*   **What it is:** A browser-based, offline-capable educational lab called "esp-labs-web" for learning about the ESP32-S3.
*   **How it works technically:** It's a web application that consolidates datasheets, pinout diagrams, tutorials, and firmware files into a single interface. It features interactive widgets and code tours. A companion repository, "esp-labs," provides the firmware and content for the learning experience.
*   **Standout Details:**
    *   **Chip:** ESP32-S3.
    *   **Software Stack:** Browser-based application.
    *   **Features:** Works offline, includes interactive widgets and code tours.
*   **Why a Maker Cares:** It solves the common problem of having dozens of tabs and PDFs open when learning a new chip. By packaging everything into one offline tool, it creates a focused and portable learning environment.

**10. Tesserae Turns E-Ink Panels Into Thin Clients**

*   **What it is:** A client-server system for driving multiple e-ink displays from a single server.
*   **How it works technically:** A central Tesserae server renders HTML content (authored in a browser) into a calibrated frame ready for an e-ink panel. Client devices, which can be Raspberry Pi or battery-powered ESP32 boards, fetch these packed bytes, report their status, refresh their screen, and go to sleep.
*   **Standout Details:**
    *   **Chips:** ESP32, Raspberry Pi.
    *   **Displays:** E-ink panels.
    *   **Architecture:** Client-server model. The server does the heavy lifting (rendering), while clients are lightweight.
*   **Why a Maker Cares:** This is an efficient architecture for smart home dashboards or status displays. It offloads processing from battery-powered microcontrollers, allowing for longer life and simpler client code, while managing a whole house of displays from one place.

**11. ESP32 Digital Tube-Sound Processor**

*   **What it is:** A compact digital audio processor that emulates the "warm" sound of vacuum tubes.
*   **How it works technically:** An ESP32 runs the audio processing algorithms. A WM8960 codec handles audio input and output. The user interface consists of a color display and three rotary encoders. The software separates standard tone controls from the nonlinear harmonic processing that creates the "tube sound" and includes features like presets and spectral analysis.
*   **Standout Details:**
    *   **Chips:** ESP32, WM8960 audio codec.
    *   **Interface:** Color display, 3 rotary encoders.
    *   **Software:** Reuses hardware/software from a previous parametric equalizer project; performs spectral analysis of the second harmonic.
*   **Why a Maker Cares:** It's a deep dive into digital signal processing (DSP) on a hobbyist-friendly platform. The project demonstrates how to create complex audio effects digitally, including visual feedback on the process.

**12. Build a $10 ESP32-C3 NFC Access Controller**

*   **What it is:** "Prismo" is a low-cost, self-hosted NFC access controller for things like doors or machinery.
*   **How it works technically:** An ESP32-C3 reads the UID from an NFC card via a PN532 module. It then checks for authorization by communicating with a server over MQTT. Based on the response, it provides local feedback with an LED and buzzer and switches a relay. The whole project is built on a single-layer PCB designed to be easy for makers to fabricate.
*   **Standout Details:**
    *   **Chips:** ESP32-C3, PN532 (NFC reader).
    *   **Protocol:** MQTT.
    *   **Cost:** Approximately $10 in parts.
    *   **Hardware:** Single-layer, maker-friendly PCB.
*   **Why a Maker Cares:** This is an extremely accessible and practical security project. The low cost, use of standard protocols like MQTT, and maker-friendly PCB design make it a perfect template for anyone wanting to build their own NFC access system.

### **IoT**

**13. Turn an Android Tablet Into a Home Assistant Hub**

*   **What it is:** "Kiosk Satellite" is an app that repurposes an old Android tablet into a multi-function Home Assistant controller.
*   **How it works technically:** The app acts as a frontend for Home Assistant, providing dashboards, voice control, media controls, and timers. It can also use the tablet's built-in sensors (like the camera) as sensors within Home Assistant. An optional companion service, "Ground Control," can be run nearby to handle heavier voice processing tasks.
*   **Standout Details:**
    *   **Platform:** Android tablet.
    *   **Integration:** Home Assistant.
    *   **Features:** Voice satellite, camera sensor, music screen, dashboards.
*   **Why a Maker Cares:** It’s a fantastic way to upcycle old electronics. Instead of buying a dedicated smart display, makers can use a device they already own to create a powerful, customized smart home interface.

**14. Migrating ESP32 Devices to Hybrid Post Quantum TLS**

*   **What it is:** A workshop project showing how to upgrade an ESP32's security from classical TLS to a hybrid post-quantum cryptography (PQC) version.
*   **How it works technically:** An ESP32 initially connects using classical TLS. A signed firmware image is then sent over-the-air (OTA) which enables hybrid ML-KEM TLS. The backend uses a custom Mosquitto bridge to connect the device to AWS IoT Core, with cloud services managing certificates, builds, and migration status.
*   **Standout Details:**
    *   **Chip:** ESP32.
    *   **Protocol:** Hybrid ML-KEM TLS.
    *   **Software Stack:** Custom Mosquitto bridge, AWS IoT Core.
*   **Why a Maker Cares:** This is a forward-looking project that tackles next-generation security for the IoT. It gives makers a hands-on look at what will be required to secure devices against future quantum computing threats.

**15. Bring Vehicle Telemetry into Home Assistant**

*   **What it is:** "Car 2 Home" is a custom Home Assistant integration that brings live data from your car into your smart home.
*   **How it works technically:** An ELM327 OBD-II adapter plugs into the car and sends data to a companion phone app. The phone app then maintains a persistent WebSocket connection to the Home Assistant integration on the local network, feeding it live engine data, trip info, location, and diagnostic codes.
*   **Standout Details:**
    *   **Hardware:** ELM327 OBD-II adapter.
    *   **Protocol:** Persistent WebSocket (no MQTT or cloud relay).
    *   **Integration:** Custom Home Assistant integration.
*   **Why a Maker Cares:** It bridges the gap between their car and their smart home without relying on a third-party cloud service. This local-first approach is highly appealing to makers focused on privacy and control.

**16. Local EV Charging Control for Home Assistant**

*   **What it is:** A Home Assistant integration that provides local network control over a Tuya-based EV charger.
*   **How it works technically:** The integration uses the `tinytuya` library to communicate with the charger directly over the LAN. The core of the project is the control logic, which makes charging decisions based on various inputs: grid meter readings, solar power surplus, home battery state, electricity tariffs, and safety limits.
*   **Standout Details:**
    *   **Hardware:** Tuya-based EV charger.
    *   **Software:** Home Assistant integration using `tinytuya`.
    *   **Protocol:** Local LAN communication (no cloud).
*   **Why a Maker Cares:** This puts the "smart" in smart charging. Instead of relying on a manufacturer's app, a maker can build sophisticated, customized automations that optimize charging based on their specific home energy setup, saving money and using green energy more effectively.

### **Raspberry Pi**

**17. Momo Turns a Pi Into a Puppy**

*   **What it is:** "Momo" is a Raspberry Pi 5-powered desk companion shaped like a German Shepherd puppy.
*   **How it works technically:** A Raspberry Pi 5 runs the core logic. The build includes a custom 3D printed shell, an HDMI display for the face, a microphone for voice commands, and an I2S audio interface for puppy sounds. It integrates with cloud services for voice AI and also has a retro-gaming mode.
*   **Standout Details:**
    *   **Chip:** Raspberry Pi 5.
    *   **Hardware:** Custom printed shell, HDMI display, microphone, I2S audio.
    *   **Software:** Integrates voice AI via cloud services, includes a retro-gaming mode.
*   **Why a Maker Cares:** It's a highly charismatic project that combines 3D printing, electronics, AI services, and emulation into a single, polished device. It’s a great example of a "desk bot" with a lot of personality.

**18. SIMUT: Pico W Telemetry With Custom Sensor Hardware**

*   **What it is:** "SIMUT" is an open-source environmental monitoring platform based on the Raspberry Pi Pico W.
*   **How it works technically:** The system is built around a custom PCB with 16 sensor slots. The Pico W or Pico 2 W board collects data and provides a local display. The project's repository is comprehensive, including firmware, KiCad board files, command-line tools, language packs, and fabrication outputs.
*   **Standout Details:**
    *   **Chips:** Raspberry Pi Pico W, Pico 2 W.
    *   **Hardware:** Custom PCB with 16 sensor slots.
    *   **Project Scope:** Open-source repository includes firmware, KiCad files, CLI tools, and more.
*   **Why a Maker Cares:** This isn't just a one-off project; it's a full-fledged, extensible platform. Makers can use it as a robust starting point for their own custom, multi-sensor monitoring systems.

**19. Turn a Pico 2 W into a Home Assistant Sensor**

*   **What it is:** A simple project to make a Raspberry Pi Pico 2 W a native sensor in Home Assistant using ESPHome.
*   **How it works technically:** A short ESPHome YAML configuration file is created to define sensors for the Pico's chip temperature, Wi-Fi signal strength, uptime, and LED state. This configuration is flashed once via USB, and all subsequent updates can be done wirelessly (over-the-air).
*   **Standout Details:**
    *   **Chip:** Raspberry Pi Pico 2 W (requires a 'W' model).
    *   **Software Stack:** ESPHome, Home Assistant.
    *   **Process:** One-time USB flash, then wireless updates.
*   **Why a Maker Cares:** This is arguably the easiest way to create a custom Wi-Fi sensor for Home Assistant. The power of ESPHome on the Pico W platform dramatically lowers the barrier to entry for creating custom smart home devices.

**20. OpenScreens Turns Apple Devices into Raspberry Pi Remotes**

*   **What it is:** An app that lets you control a Raspberry Pi's desktop from an iPhone, iPad, or Mac.
*   **How it works technically:** The app acts as a VNC client. After enabling the VNC server on the Raspberry Pi, you add the Pi's address and credentials to the OpenScreens app. It can connect over the local network, or securely through an SSH tunnel or Tailscale.
*   **Standout Details:**
    *   **Platform:** iOS, iPadOS, macOS.
    *   **Protocol:** VNC, with options for SSH or Tailscale tunneling.
    *   **Features:** Touch gestures, trackpad mode, saved sessions.
*   **Why a Maker Cares:** It provides a polished and practical way to manage headless or remote Raspberry Pi projects from the Apple ecosystem, which is often a missing piece for many users.

**21. A 62 mm Raspberry Pi Pico Macintosh**

*   **What it is:** "pico-mac-nano" is a tiny, 62mm tall, functional Macintosh 128K emulator powered by an RP2040.
*   **How it works technically:** A Raspberry Pi Pico Zero (with RP2040) runs the Macintosh emulator. It uses a custom PCB to connect a portrait TFT display, a micro-SD card for storage (disk images), a USB port for input, and an audio output. All components fit inside a miniature 3D printed Macintosh case.
*   **Standout Details:**
    *   **Chip:** RP2040 (on a Pico Zero).
    *   **Hardware:** Custom PCB, portrait TFT screen, micro-SD storage.
    *   **Size:** 62 mm tall.
    *   **Project Scope:** Includes firmware, source code, board files, disk images, and printable parts.
*   **Why a Maker Cares:** This is a masterclass in miniaturization and retro-computing. It's a challenging and rewarding project for those who enjoy working with tight physical and computational constraints.

### **Robotics**

**22. Build a Sim Racing Seatbelt Tensioner**

*   **What it is:** An open-source, dual-channel force-feedback system for a sim racing rig that tightens the seatbelts during braking.
*   **How it works technically:** Two ESP32-S3 boards control iSV57 servos attached to linear modules. The system gets braking data from the SimHub software. It uses sensorless homing and current monitoring for motion control, eliminating the need for external limit switches.
*   **Standout Details:**
    *   **Chips:** ESP32-S3 boards (plural).
    *   **Hardware:** iSV57 servos, linear modules.
    *   **Software:** Uses data from SimHub.
    *   **Features:** Dual-channel (both shoulder belts), sensorless homing, automatic parking.
*   **Why a Maker Cares:** This adds a powerful layer of physical immersion to a sim racing setup. The use of sensorless homing is a sophisticated motor control technique that makers can learn from.

**23. MARS Builds One Rover Base for Many Jobs**

*   **What it is:** "MARS" is a modular rover prototype with a base platform for driving and separate, swappable payload modules for different tasks.
*   **How it works technically:** The base has two decks and four motors. An Arduino Uno handles Bluetooth-based driving control and basic obstacle stopping. Separate payload modules using a Raspberry Pi and another Arduino Nano add video streaming and environmental sensing capabilities.
*   **Standout Details:**
    *   **Chips:** Arduino Uno (base), Raspberry Pi, Arduino Nano (payloads).
    *   **Architecture:** Modular design with separate controllers for driving and payloads.
    *   **Status:** The design is functional but noted as unfinished regarding shared power, data links, and autonomous navigation.
*   **Why a Maker Cares:** This is a great example of a modular robotics design. It shows how to separate concerns, allowing a team or individual to work on different functions (like driving vs. sensing) independently.

**24. Lyapunov Unifies Robot Scenes, Physics, and Camera Data**

*   **What it is:** "Lyapunov" is a desktop software workspace for developing robot models, from scene setup and physics simulation to camera calibration.
*   **How it works technically:** It's an Apache-2.0 licensed software tool that combines file management, code editors, terminals, physics simulation, image annotation, and dataset tools into one unified environment. It is noted as being software-heavy and may require separate setup for advanced rendering or hardware integration.
*   **Standout Details:**
    *   **Type:** Desktop software workspace (not a hardware build).
    *   **License:** Apache-2.0.
    *   **Function:** Unifies simulation, control, and data capture/management for robotics development.
*   **Why a Maker Cares:** This is a tool for the "brains" side of robotics. It helps bridge the gap between simulation and the real world, providing a structured environment for developing and testing robot software before deploying it on physical hardware.