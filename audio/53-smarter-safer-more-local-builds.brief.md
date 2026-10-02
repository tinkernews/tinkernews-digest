**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-09-15
**SUBJECT:** Episode Brief: TinkerNews Issue #53

Here is the detailed research brief for our next episode covering TinkerNews Issue #53. The theme is builds that are smarter, safer, or more locally controlled. Every project from the newsletter is broken down below with its core function, technical details, and the key takeaway for our maker audience. All information is taken directly from the source material.

---

### **Episode Brief: TinkerNews #53**

#### **Arduino**

**1. An Offline Arduino Agent That Understands Plain English**

*   **What it is:** A project that controls Arduino-connected hardware based on plain-English text commands, processed entirely on-device without an internet connection.
*   **How it works technically:** A user types a natural language instruction into an Arduino App Lab project. A local language model running on the Arduino UNO Q board processes this instruction and then directs connected Modulino sensors and outputs to perform the requested action.
*   **Standout Details:**
    *   **MCU:** Arduino UNO Q
    *   **Software:** Arduino App Lab
    *   **Hardware:** Modulino sensors and outputs
    *   **Key Feature:** On-device, local language model. Requires no internet access or API keys.
*   **Why a Maker Cares:** This demonstrates a significant shift from traditional coding. Instead of rewriting and flashing new firmware to change a device's behavior, a maker can simply provide a new sentence. It's a practical entry point into local AI for hardware control.

**2. Arduino Two-Axis Level With Zero Reference**

*   **What it is:** A handheld, digital two-axis level that can store a reference angle from one surface to precisely match it on another.
*   **How it works technically:** An ADXL345 accelerometer continuously measures gravity's pull to determine pitch and roll angles. An Arduino Nano reads this data, processes it, and displays the pitch and roll on an OLED screen. A "ZERO" button allows the user to store the current angle as a reference point.
*   **Standout Details:**
    *   **MCU:** Arduino Nano
    *   **Sensor:** ADXL345 (3-axis accelerometer)
    *   **Display:** OLED
    *   **Functionality:** Can compare two surfaces, even if both are intentionally sloped, by storing a zero reference.
*   **Why a Maker Cares:** It's a more advanced measurement tool than a standard bubble or digital level. It solves the specific problem of transferring or matching an exact angle between two separate objects, which is common in fabrication, alignment, and assembly tasks.

#### **3D Printing**

**3. MedusaHC: Open-Source Python Toolchanger for Klipper**

*   **What it is:** An open-source project that adds automatic hotend (tool) changing capabilities to a 3D printer running Klipper firmware.
*   **How it works technically:** It is a combination of a mechanical system and a Python-based controller. The controller software coordinates the entire tool-changing sequence: picking up a tool, parking the old one, feeding filament, priming, cleaning, and performing sensor checks, while integrating with Klipper's existing command structure.
*   **Standout Details:**
    *   **Software Stack:** Klipper (printer firmware), Python (controller)
    *   **Status:** Beta project
    *   **Requirements:** Involves significant mechanical work, calibration, and following the repository's installation guide.
*   **Why a Maker Cares:** This provides a non-proprietary, open-source pathway to multi-material or multi-tool 3D printing. It's targeted at experienced makers who are comfortable with mechanical modifications and calibration to achieve advanced functionality on their Klipper-based machines.

**4. Low-Cost 3D-Printed AirFlow Microreactor**

*   **What it is:** A low-cost, open-source device designed to hold LAMP (Loop-mediated isothermal amplification) reactions at a stable, elevated temperature.
*   **How it works technically:** A 3D-printed chamber houses the reaction. Forced hot air is used as the heating mechanism. An Arduino controller manages the system to maintain a near-steady temperature required for the biological reaction.
*   **Standout Details:**
    *   **Control:** Arduino
    *   **Cost:** Approximately £100
    *   **Technology:** Uses a printed chamber and forced hot air for thermal regulation.
    *   **Target Use:** LAMP reactions (a method for DNA amplification).
    *   **Availability:** Presented as an evolving open build on the Biomaker project hub with downloadable files.
*   **Why a Maker Cares:** This project makes DIY biology and home-lab science more accessible. It's a practical, affordable tool for classrooms, community labs, and individual researchers who need precise temperature control for biotech experiments without expensive lab equipment.

#### **ESP32**

**5. Hestia32: An Open Thermostat for Multi-Stage HVAC**

*   **What it is:** An open-source, locally-controlled smart thermostat designed to be repairable and to work with a variety of HVAC systems, including multi-stage ones.
*   **How it works technically:** An ESP32-C5 microcontroller is the core. It gets temperature and humidity data from an SHT45 sensor. It controls the HVAC system via configurable relays. User interaction is through a touchscreen, and it integrates with home automation systems via MQTT.
*   **Standout Details:**
    *   **MCU:** ESP32-C5
    *   **Sensor:** SHT45
    *   **Features:** Touchscreen, configurable relays, Over-The-Air (OTA) updates.
    *   **Protocols:** Supports MQTT now. Thread, Matter, and Zigbee are planned.
    *   **Core Principle:** No cloud subscription required; local control is central.
    *   **Status:** Project is in development.
*   **Why a Maker Cares:** It's a direct answer to proprietary, cloud-dependent smart thermostats. It offers repairability, local control, and compatibility with open home automation platforms like Home Assistant. Support for multi-stage systems makes it applicable to more complex home setups.

**6. Turn a Sonoff NSPanel into Local Control**

*   **What it is:** A project to modify a commercial Sonoff NSPanel EU smart switch, replacing its stock firmware to integrate it as a local controller with Home Assistant.
*   **How it works technically:** The ESP32 inside the Sonoff NSPanel is flashed with ESPHome firmware. This exposes the panel's hardware—touchscreen, two physical buttons, two relays, and a temperature sensor—directly to Home Assistant. Home Assistant then becomes the local controller for the panel.
*   **Standout Details:**
    *   **Hardware:** Sonoff NSPanel EU (which contains an ESP32).
    *   **Software Stack:** ESPHome (firmware on device), Home Assistant (local controller).
    *   **Safety Warning:** Involves working directly with 240V mains terminals, requiring serious electrical safety precautions.
*   **Why a Maker Cares:** This is a classic maker hack: taking an affordable, polished piece of commercial hardware and liberating it from its manufacturer's ecosystem. It provides a professional-looking, wall-mounted user interface for a fully local, open-source smart home.

#### **IoT**

**7. Sync Home Assistant Lights With the Sun (Adaptive Lighting)**

*   **What it is:** A Home Assistant integration that automatically adjusts the color temperature and brightness of smart lights throughout the day to mimic natural sunlight.
*   **How it works technically:** The "Adaptive Lighting" integration uses Home Assistant's built-in sun entity, which tracks the sun's position. Based on this data, it adjusts connected lights to be cooler and brighter during the day, and warmer and dimmer in the evening. Manual overrides are still possible.
*   **Standout Details:**
    *   **Platform:** Home Assistant
    *   **Data Source:** Home Assistant's `sun` integration.
    *   **Hardware:** Works with existing smart lights; no custom hardware is needed.
*   **Why a Maker Cares:** It's a pure software solution that makes a smart home feel more natural and less static. It's a high-impact automation that requires no new hardware, just configuration within an existing Home Assistant setup.

**8. Turning Huawei Solar into Home Assistant Data**

*   **What it is:** A Home Assistant integration for pulling detailed data from supported Huawei Solar inverters.
*   **How it works technically:** The integration communicates with the Huawei Solar equipment over the local network using the Modbus protocol. It reads out various data points and functions, presenting them as standard Home Assistant "entities" that can be used in dashboards and automations.
*   **Standout Details:**
    *   **Platform:** Home Assistant
    *   **Protocol:** Modbus
    *   **Compatibility:** Requires supported Huawei Solar hardware and a reachable network interface.
    *   **Configuration:** Setup requires correct addressing and setting sensible polling intervals.
*   **Why a Maker Cares:** For makers with this specific solar hardware, it unlocks a wealth of data beyond a single power generation number. This detailed information can be used for more sophisticated energy monitoring, dashboarding, and creating automations to optimize energy usage.

**9. Build Long-Running ESP32 Sensor Nodes with Deep Sleep**

*   **What it is:** A practical guide explaining the techniques required to maximize the battery life of ESP32-based remote sensor nodes.
*   **How it works technically:** The guide outlines a "wake, measure, transmit, sleep" operational pattern. It details the technical considerations involved, including different wake-up sources, retaining state across sleep cycles, the energy cost of wireless transmissions, and the impact of board-level current leakage on overall runtime.
*   **Standout Details:**
    *   **MCU:** ESP32
    *   **Core Concept:** Deep Sleep power management.
    *   **Topics Covered:** Wake sources, retained state, wireless energy costs, board leakage current.
    *   **Application:** Aimed at battery-powered remote devices like soil monitors or weather stations.
*   **Why a Maker Cares:** This addresses a fundamental challenge in DIY IoT: battery life. It moves beyond just the MCU's sleep current datasheet value to the practical, real-world factors that determine whether a remote sensor will last for weeks or months, teaching essential low-power design skills.

#### **Raspberry Pi**

**10. Raspberry Pi 5 UPS with Modular Battery Protection**

*   **What it is:** An open-hardware Uninterruptible Power Supply (UPS) for the Raspberry Pi 5 that uses common, removable NP-F style batteries.
*   **How it works technically:** The board manages power from a USB-PD input and the attached NP-F batteries. In case of a power outage, it seamlessly switches to battery power. It includes firmware to monitor the state and can trigger a safe shutdown of the Pi. The project includes an OLED for status display.
*   **Standout Details:**
    *   **Target:** Raspberry Pi 5
    *   **Power Input:** USB-PD
    *   **Battery Type:** Removable NP-F batteries.
    *   **Features:** OLED display, safe shutdown firmware, 3D-printed enclosure.
    *   **Status:** Open hardware with documented limits.
*   **Why a Maker Cares:** It provides a complete, well-documented solution for power resilience on a Pi 5. Using standard, swappable NP-F batteries is a great feature for projects that need both uptime during outages and the ability to run portably for extended periods by swapping batteries.

**11. PEBBLE: A Raspberry Pi Recorder in a Rock**

*   **What it is:** A self-contained, portable voice recorder built around a Raspberry Pi, housed in a small, pebble-shaped enclosure.
*   **How it works technically:** This project integrates all the necessary components for an audio recorder: wiring a microphone to the Pi, configuring the software for audio capture, managing file storage on the Pi, and powering it all from a portable battery.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi
    *   **Function:** Portable audio recorder.
    *   **Scope:** Covers microphone wiring, audio capture software, storage, battery power, controls, and enclosure design.
*   **Why a Maker Cares:** It's a perfect case study in turning a general-purpose computer like the Raspberry Pi into a specialized, single-purpose handheld device. It forces the maker to solve problems of power, user interface, and physical form factor.

**12. Build an OpenFlight Controller with Raspberry Pi**

*   **What it is:** A flight electronics controller project based on a Raspberry Pi.
*   **How it works technically:** The project uses a Raspberry Pi for computation. It involves GPIO wiring for controls, UART serial communication for connecting to other peripherals, and custom software for diagnostics. A key part of the project is designing a custom enclosure to fit all the components reliably.
*   **Standout Details:**
    *   **Platform:** Raspberry Pi
    *   **Interfaces:** GPIO, UART serial communication.
    *   **Scope:** A complete flight electronics package, including hardware and enclosure.
    *   **Status:** Described as an "active build," suggesting it's a work-in-progress where makers need to verify specific parts and steps.
*   **Why a Maker Cares:** This is an ambitious project for those interested in avionics or drone building. It shows how to use the Pi's computing power and I/O in a demanding application where reliable communication and physical integration are critical.

**13. Build an Open-Hardware IP-KVM for Remote Computer Control**

*   **What it is:** ESPKVM is an open-hardware IP-KVM (Keyboard, Video, Mouse over IP) that allows remote control of a computer, even if it's stuck or has no network connection.
*   **How it works technically:** The system uses custom hardware boards designed around an HDMI capture chip (for video) and a USB interface (for emulating a keyboard and mouse). This hardware is networked, allowing a user to see the remote computer's screen and send keyboard/mouse inputs over the network.
*   **Standout Details:**
    *   **Function:** IP-KVM (remote video, keyboard, mouse).
    *   **Hardware:** Custom boards with HDMI capture and USB capabilities.
    *   **Availability:** Schematics and board targets are available.
    *   **Status:** Described as a useful starting point, "pending hardware verification."
*   **Why a Maker Cares:** This is a powerful tool for anyone managing remote computers or a home lab. Building an open-hardware version provides a deep understanding of video capture and USB HID protocols, offering a non-commercial alternative to expensive enterprise KVMs.

#### **Robotics**

**14. Build an Open-Source ADS-B Receiver for Nearby Aircraft**

*   **What it is:** ADSBee is a compact, open-source, low-power receiver for decoding ADS-B signals from aircraft.
*   **How it works technically:** The custom board is designed specifically for 1090 MHz reception, which is the frequency used for ADS-B broadcasts. It handles both the radio reception and the decoding of the aircraft data packets on a single low-power board.
*   **Standout Details:**
    *   **Function:** ADS-B Receiver.
    *   **Frequency:** 1090 MHz.
    *   **Design:** Open-source, low-power, compact board.
    *   **Key Advantage:** Does not require the typical combination of a Raspberry Pi and a separate SDR (Software-Defined Radio) dongle.
*   **Why a Maker Cares:** It offers a more integrated, power-efficient, and portable solution for aircraft tracking compared to the common Pi+SDR setup. This makes it ideal for portable trackers, custom data displays, or remote, field-deployed monitoring stations.

---
**End of Brief**