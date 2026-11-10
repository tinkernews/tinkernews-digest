Here is the detailed episode brief for the podcast hosts.

***

### **Episode Brief: TinkerNews Issue #61**

**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-11-10
**SUBJECT:** Episode Notes for TinkerNews Issue #61

Hi team,

Here is the brief for our next episode covering TinkerNews #61. The theme is practical edge computing. We have a great mix of robotics, local AI on small devices, smart home integrations that prioritize local control, and some classic hardware hacking and repurposing.

Please stick to the facts provided. I've broken down every build with the key technical details and the "so what" for our maker audience.

---

### **Robotics**

#### **Browser-Controlled XGO Duck on Arduino Uno Q**

*   **What it is:** A software runtime that allows you to control an XGO Duck quadruped robot from a web browser, using an Arduino Uno Q as the brain.
*   **How it works technically:** The system uses the Uno Q's Linux side to run Python for high-level control and pre-learned motion policies in ONNX format. The STM32 microcontroller side handles the real-time feedback loops. A browser acts as the user interface.
*   **Standout Details:**
    *   **Hardware:** Arduino Uno Q, XGO Duck.
    *   **Software Stack:** Python, STM32 sketch, ONNX motion policies.
    *   **Functionality:** The runtime manages calibration, motion recovery, skating movements, servo safety checks, and provides diagnostics.
*   **Why a Maker Cares:** This is a complete, practical software stack for a complex robot. It’s a great example of a hybrid computing approach, using a Linux environment for complex logic (AI models) and a microcontroller for deterministic, real-time control.

#### **$1.50 FOC Board for a Tiny 10:1 Robot Joint**

*   **What it is:** A very low-cost, compact robotic joint module.
*   **How it works technically:** It combines a small brushless gimbal motor with a custom-designed, four-layer Field-Oriented Control (FOC) board. A 3D-printed 10:1 planetary gearbox provides torque multiplication.
*   **Standout Details:**
    *   **Hardware:** 1503 brushless gimbal motor, a four-layer FOC board (~$1.50), 3D-printed 10:1 gearbox.
    *   **Project Status:** The hardware design is open-source. However, the firmware is currently open-loop and requires significant configuration to function as a dependable servo.
*   **Why a Maker Cares:** This project hits a key maker goal: creating capable robotics components for an extremely low cost. It's a great open hardware starting point, but also a realistic look at the challenges of firmware development—the hardware is just one part of the problem.

#### **MOSS: An Open-Source Litter-Picking Rover**

*   **What it is:** MOSS (Metro-cross Open-Source Scavenger) is a 3D-printed, tracked rover designed to follow a person and pick up small pieces of litter with a robotic arm.
*   **How it works technically:** The current prototype is teleoperated for driving and pick-and-drop manipulation. The project is designed to be extensible.
*   **Standout Details:**
    *   **Hardware:** 3D-printed tracked chassis, robotic arm.
    *   **Flexibility:** The project supports several different computer choices and provides simulation tools to help development.
    *   **Project Status:** The hardware files are open-source. The current version demonstrates teleoperation.
*   **Why a Maker Cares:** This is a substantial, real-world robotics project for experienced makers. The availability of open hardware files, simulation tools, and flexibility in the choice of computing hardware makes a complex build like this more achievable.

---

### **Arduino**

#### **Connecting the UNO Q’s Linux and STM32 Sides**

*   **What it is:** A foundational tutorial demonstrating how to pass data between the Debian Linux processor and the STM32 microcontroller on the Arduino UNO Q.
*   **How it works technically:** A potentiometer on an analog pin (A5) is read by the STM32. This value is sent to a Python script on the Linux side using the "Bridge" library. The Python script then sends a command back to the STM32 to set the brightness of the built-in LED. It also shows how to add browser-based control using a WebSocket.
*   **Standout Details:**
    *   **Hardware:** Arduino UNO Q.
    *   **Software API:** Demonstrates the Bridge library, specifically the `call()`, `notify()`, and `provide_safe()` functions.
    *   **Protocols:** WebSockets.
*   **Why a Maker Cares:** For anyone with an Arduino UNO Q, this is essential reading. It demystifies the board's main feature: communication between its two different processors. It provides clear guidance on which communication functions to use for different scenarios.

#### **An Arduino UNO Q Runs a Local AI Thermostat**

*   **What it is:** A proof-of-concept AI thermostat that runs a small language model entirely locally on an Arduino UNO Q.
*   **How it works technically:** A Python script on the Uno Q's Linux side runs the local AI model. The model is given a limited set of "tools" to interact with the hardware—in this case, reading a simulated temperature and controlling an LED fan. The actual hardware control is handled deterministically by a sketch on the STM32 side.
*   **Standout Details:**
    *   **Hardware:** Arduino UNO Q, LED fan.
    *   **Software Stack:** Python, a small language model, STM32 sketch.
    *   **Metrics:** The project measures and reports on startup delay, response speed, memory usage, and model size.
*   **Why a Maker Cares:** This is a perfect example of practical, safe edge AI. It shows how to give an AI model agency over hardware while keeping a deterministic microcontroller in charge for safety. The included performance metrics are invaluable for anyone looking to run AI on constrained devices.

---

### **DIY Electronics / ESP32**

#### **Mecha Desk Buddy with Touchscreen Face**

*   **What it is:** A 3D-printed desktop organizer shaped like a small mecha-robot, featuring storage compartments and an animated face on a touchscreen.
*   **How it works technically:** An ESP32-S3 microcontroller drives a 2.8-inch touchscreen. The user interface, which includes blinking eyes and six different facial expressions, is created using the LVGL 9 graphics library running in the Arduino environment.
*   **Standout Details:**
    *   **Hardware:** ESP32-S3, 2.8-inch touchscreen.
    *   **Construction:** Composed of 33 individual 3D-printed parts.
    *   **Software:** Arduino, LVGL 9.
    *   **Functionality:** Has storage for a phone, pens, SD cards, and circuit boards.
*   **Why a Maker Cares:** It's a fantastic blend of practical 3D printing and expressive electronics. It serves as a great showcase for building polished graphical interfaces on an ESP32 using the powerful and open-source LVGL library.

#### **Marelleo: An ESP32 Story Box for NFC Figurines**

*   **What it is:** A kid-friendly box that plays a story, song, or radio station when a specific NFC-tagged figurine is placed on it.
*   **How it works technically:** An ESP32 detects an NFC tag, connects to Wi-Fi, and plays the associated audio file. The project documentation covers the entire design evolution.
*   **Standout Details:**
    *   **Hardware:** ESP32, NFC reader.
    *   **Protocols:** NFC, Wi-Fi.
    *   **Design Journey:** The write-up details the progression from breadboard to perfboard and finally to a custom PCB, highlighting real-world considerations like battery safety, mechanical failure points, and recovery testing.
*   **Why a Maker Cares:** This project provides a valuable look at the entire making process, beyond just a final schematic. The focus on iterative design and solving practical problems makes it a great case study for moving a project from a fragile prototype to a robust, usable object.

#### **Kube32: `kubectl` for ESP32 Clusters**

*   **What it is:** A framework that lets you manage a cluster of ESP32s using standard Kubernetes tooling like `kubectl` to deploy WebAssembly apps.
*   **How it works technically:** The system uses one ESP32-S3 with PSRAM as a "control plane" to manage multiple "worker" boards (like the M5Stack Cardputer). Kube32 treats the hardware on the worker nodes—such as displays, sensors, and inputs—as manageable resources within the cluster.
*   **Standout Details:**
    *   **Hardware:** Requires an ESP32-S3 with PSRAM for the control plane.
    *   **Software Stack:** Kube32, `kubectl`, WebAssembly (Wasm).
    *   **Tools:** Includes a simulator and practical examples to lower the barrier to entry.
*   **Why a Maker Cares:** This is a mind-bending project that brings high-level cloud-native orchestration concepts down to the microcontroller level. It’s for advanced makers interested in distributed systems, IoT fleet management, and the future of embedded software.

#### **Browser-Controlled ESP8266 Relay**

*   **What it is:** A beginner-friendly project to switch a relay on and off from a web browser over your local Wi-Fi network.
*   **How it works technically:** A NodeMCU ESP8266 board hosts a simple webpage. When a user on the same 2.4 GHz network accesses the page, they can click a button to toggle a relay connected to the board's GPIO pins.
*   **Standout Details:**
    *   **Hardware:** NodeMCU ESP8266, one relay, one status LED.
    *   **Software:** A short and simple Arduino sketch.
    *   **Limitations:** The project is clear about its limits: it's not secure, it's for local access only, and it warns about the dangers of wiring mains voltage.
*   **Why a Maker Cares:** This is the quintessential "Hello, World!" of IoT. It’s a perfect first project for anyone new to the ESP8266, and the explicit safety and security warnings make it a responsible and educational starting point.

#### **ESP32-S3 Rotary Universal Timer**

*   **What it is:** A physical kitchen-style timer using a rotary encoder for input and a circular touchscreen for display.
*   **How it works technically:** Built on a CrowPanel (ESP32-S3), the project uses a rotary encoder to set the time across four different scales. The circular display is updated smoothly using framebuffer drawing techniques. An external buzzer provides audible alerts.
*   **Standout Details:**
    *   **Hardware:** CrowPanel (ESP32-S3), rotary encoder, circular display, external buzzer.
    *   **Software:** Arduino. It requires specific ESP32 and graphics library settings. The key to the smooth display is framebuffer drawing.
*   **Why a Maker Cares:** It's a polished and satisfying user interface project. The combination of a rotary encoder and a circular display is an elegant alternative to standard buttons and square screens, and the use of framebuffer drawing is a great technical tip for anyone doing graphics on microcontrollers.

#### **Open ESP32-S3 Board Designed in KiCad**

*   **What it is:** A complete, open-source set of design files for a custom ESP32-S3 development board.
*   **How it works technically:** This is a design project, not a finished build. The repository contains all the files needed to inspect the design and have the PCB fabricated.
*   **Standout Details:**
    *   **Chip:** Based on the Espressif ESP32-S3-WROOM-1-N8R8 module.
    *   **Design Files:** The repo includes the KiCad schematic and PCB layout, custom libraries, Bill of Materials (BOM), Gerbers, and drill files.
    *   **Project Status:** The design phase is complete. Assembly, testing, and firmware development are the next steps.
*   **Why a Maker Cares:** This is an invaluable resource for anyone learning or doing custom PCB design. It's a complete, modern example they can study, modify, or use as a solid foundation for their own custom ESP32-S3 board.

---

### **IoT / Home Assistant**

*(Note: There are a lot of Home Assistant projects this issue. The common theme is local control and integrating non-standard hardware.)*

*   **Build a 3D Home Assistant Dashboard (NeonPlan 3D):** A software project that lets you create a 3D model of your home and see your Home Assistant devices (lights, sensors, cameras) in their physical locations. It's a more intuitive UI than standard lists.
*   **Repurpose an Old Echo for Home Assistant:** A hack that disconnects an Amazon Echo from the Alexa cloud and reroutes its far-field microphone array to Home Assistant Assist. This gives you a high-quality, local voice assistant using cheap, repurposed hardware. **Warning:** High risk of bricking the device.
*   **Build a Live 3D Smart-Home Controller (House Control):** A native Mac and iPhone app that creates a live 3D control surface from a JSON floor plan. It integrates with multiple platforms, including Home Assistant, Philips Hue, and Apple Home.
*   **Marstek Venus E Meets Home Assistant:** A hardware integration using a LilyGO T-CAN485 board to read data from a Marstek Venus E home battery over RS485 and send it to Home Assistant via ESPHome.
*   **ESP8266 Wi-Fi Bridge for Pylontech Batteries:** Another energy-monitoring project. This one uses a Wemos D1 Mini and a MAX3232 chip to bridge a Pylontech battery's RS-232 console port to Wi-Fi, sending data to Home Assistant via MQTT.
*   **SpiderBridge Puts GGS Control on Home Assistant:** This project uses a ~€10 ESP32 to intercept control of a Spider Farmer hydroponics controller. It provisions the device via Bluetooth once, then allows for fully local Wi-Fi control via MQTT in Home Assistant, bypassing the cloud.
*   **Turn a Cheap Wi-Fi Clock Into an ESP32 Display:** A hardware hack that replaces the proprietary internals of a cheap "HU-058D" Wi-Fi clock with an ESP32, turning it into a customizable display for Home Assistant data. It reuses the case and RGB LED matrix.

---

### **Raspberry Pi**

#### **A Pico 2 W Runs Its Own Tiny Game Worlds**

*   **What it is:** An experimental project where five simple video games run on a Pico 2 W, with two neural networks generating the game frames and deciding on actions in real-time.
*   **How it works technically:** It uses several advanced optimization techniques to run on the microcontroller: grid tokens for representing the game state, a reused transformer block, int8 weight quantization, and scheduling tasks across both cores of the Pico.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi Pico 2 W.
    *   **Software:** Two neural networks (transformer-based).
    *   **Performance:** Works well on very simple games but struggles with anything more complex like Pac-Man, showing the limits of the hardware.
*   **Why a Maker Cares:** This is a bleeding-edge demonstration of generative AI on a tiny, low-cost microcontroller. It showcases the types of software optimizations required to run complex models in highly constrained environments.

#### **A Raspberry Pi 5 Knowledge Box for Offline Use**

*   **What it is:** A self-contained, portable server that provides access to a vast library of digital information (Wikipedia, maps, medical guides) with no internet connection required.
*   **How it works technically:** A Raspberry Pi 5 with a fast NVMe SSD runs its own local Wi-Fi hotspot. The `HAS_PrepperDisk` software automatically downloads and serves content using tools like Kiwix and Internet-in-a-Box.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi 5, NVMe SSD.
    *   **Software:** `HAS_PrepperDisk`, Kiwix, Internet-in-a-Box.
*   **Why a Maker Cares:** This is a project with real-world utility, perfect for emergency preparedness, remote locations, or simply achieving digital self-sufficiency. It’s a modern, powerful take on the "information survival kit" idea.

#### **Raspberry Pi CRT Tracks Spacecraft in Retro Mission Console**

*   **What it is:** A data-visualization project that pulls live spacecraft telemetry and tracking data and displays it on a retro CRT monitor with a mission-control aesthetic.
*   **How it works technically:** A Raspberry Pi (a 3B+ is powerful enough) runs a Rust application called `mctl`. It fetches space data, caches it for offline replay, and uses software rendering to generate a 640x480 composite video signal for the CRT.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi 3B+, composite CRT monitor.
    *   **Software:** Written in Rust.
    *   **Features:** Multiple retro themes, interactive pages, and an unattended kiosk mode.
*   **Why a Maker Cares:** This is pure creative-tech joy. It combines a cool retro aesthetic with live, modern data. It’s a fantastic example of a unique data-viz project and a good use case for Rust on the Pi.

#### **Build a Raspberry Pi Marine Radar Display**

*   **What it is:** An open-source project called `Exodus Radar` that uses a Raspberry Pi to create a functional marine radar display.
*   **How it works technically:** The Pi connects to a Raymarine Quantum radar. Python services decode the radar data and combine it with other data streams like AIS (for ship tracking) and Signal K (for boat sensor data). The final view is rendered on an HDMI screen or in a web browser.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi, Raymarine Quantum radar.
    *   **Software:** Python services, `Exodus Radar` software.
    *   **Protocols:** Integrates Signal K and AIS data.
    *   **Disclaimer:** The project is explicitly an experimental aid and is **not** certified navigation equipment.
*   **Why a Maker Cares:** This is a high-level project showing how makers can interface with and build upon expensive, proprietary equipment in a specialized field like marine navigation. It's a serious application of DIY electronics.

#### **Build an RFID Reader for Raspberry Pi 5**

*   **What it is:** A tutorial that provides an up-to-date method for using the common RC522 RFID reader with the Raspberry Pi 5.
*   **How it works technically:** The tutorial addresses a common failure point: older guides use the `RPi.GPIO` library, which is deprecated and doesn't work well on the Pi 5. This guide correctly uses the modern `spidev` and `gpiod` libraries for SPI communication and GPIO control.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi 5, RC522 RFID module.
    *   **Voltage:** Connects at 3.3V.
    *   **Software:** Uses `spidev` and `gpiod` Python libraries.
*   **Why a Maker Cares:** This is a hugely practical piece of service journalism for the community. It solves a specific, common problem that makers are hitting right now with new hardware. It teaches the *correct*, modern way to do basic hardware interfacing on the Pi 5.