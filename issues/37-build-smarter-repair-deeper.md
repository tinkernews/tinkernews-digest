# TinkerNews #37: Build Smarter, Repair Deeper

From OBD2 tools and Modbus loggers to BLE scanners, robot vacuums, rework stations, and reverse-engineered hardware, this issue brings together practical projects for connecting…

*Issue #37 · 2026-09-07*

## 3D Printing

### Converting a K1 SE Toward K1C Features

A community discussion records one maker’s work adding K1C-like cooling and temperature sensing to a Creality K1 SE. The changes involve fans, a thermistor, wiring, firmware, and Klipper configuration—not just printed or mounted parts. It also warns against assuming K1C firmware will work safely on every K1 SE.

**Source →** [github.com](https://github.com/Guilouz/Creality-Helper-Script-Wiki/discussions/705)

## Arduino

### Add 16 I/O Pins with a PCF8575

A small PCF8575 module gives Arduino, ESP8266, or ESP32 projects 16 extra digital lines through just SDA and SCL. This hands-on setup uses LEDs and buttons to test the connection, while a library handles the I2C details and leaves the host board’s built-in pins available.

**Source →** [mischianti.org](https://mischianti.org/pcf8575-i2c-16-bit-digital-i-o-expander/)

### Build an Arduino/ESP32 OBD2 K-Line Tool

Older cars often speak K-Line instead of CAN. This Arduino/ESP32 library offers a practical starting point for connecting to those ECUs, provided you add a proper protected transceiver. The repository’s examples and source should confirm supported protocols, timing, wiring, and diagnostic commands before any vehicle connection.

**Source →** [github.com](https://github.com/muki01/OBD2_KLine_Library)

### BoatOpenIO v2: Modular Marine Gateway Main Board

BoatOpenIO v2 handles signal routing inside a four-board boat gateway. A 16:1 multiplexer sends selected analog inputs to one ADS1115 converter, while an MPU6050 watches for impacts. Socketed parts and swappable modules make repairs easier, but the board needs companion hardware before it can run.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/BoatOpenIO_v2_Main_Board_67888a6a.html)

## DIY Electronics

### ESP32 Hot-Air SMD Rework Station

Thermocouple feedback and PID control give this ESP32 hot-air station a measured way to heat surface-mount parts. Its custom PCB, MicroPython firmware, and programmable airflow make it more than a loose collection of modules, while the high-temperature hardware demands careful insulation, grounding, cooling, and power handling.

**Source →** [github.com](https://github.com/snivasms/SMD-Rework-Station)

### Reverse-Engineering a Failed Fellow Opus Grinder

Two snapped capacitor legs stopped a Fellow Opus grinder after a year of use. A careful teardown found a layered Class II enclosure, modular power and control boards, and a simple path toward diagnosis. Comparing the failed 2023 unit with its 2025 replacement also revealed useful design lessons for appliance repair.

**Source →** [hackaday.io](https://hackaday.io/project/206554-fellow-opus-2023-reverse-engineering-attempt)

### Reconstructing a Forgotten Microprofessor Sound Board

Photographs, a MAME ROM dump, and knowledge of the AY-3-8910 help rebuild an obscure Microprofessor sound board. The result is a useful KiCad schematic and annotated software, not a finished replica. Missing manuals still leave its interface and routines partly unverified, but the work preserves valuable hardware clues.

**Source →** [hackaday.io](https://hackaday.io/project/206553-sgb-mpf-i-sound-generation-board-reconstruction)

### OOMWOO: A Local, Open Robot Vacuum

OOMWOO treats a robot vacuum as a complete maker-built system: 3D-printed parts, LiDAR, Raspberry Pi computing, microcontrollers, ROS2, and Home Assistant work together without required cloud services. It remains an early-development project, though, with full build instructions planned for Fall 2026 rather than a ready-made weekend kit.

**Source →** [github.com](https://github.com/makerspet/oomwoo)

## ESP32

### ESP32-S3 Retrofit for Safer OpenTherm Control

A LOLIN S3 Mini adds Wi-Fi, HTTP, REST, MQTT, and browser control to a PIC-based NodoShop OpenTherm Gateway. This guide checks the hardware, flashes the right firmware, verifies heating data on the local network, and adds optional remote HTTP access only after local testing is complete.

**Source →** [localtonet.com](https://localtonet.com/blog/flash-otgw-firmware-esp32-s3-localtonet)

## IoT

### Build a Pocket BLE Privacy Scanner with an M5Stack

A BLE radio can reveal device names and other details before any pairing happens. GhostBLE turns that lesson into a pocket tool: an M5Stack scans nearby advertisements, shows devices on its display, and flags privacy concerns, giving makers a practical way to inspect their own homes, labs, and prototypes.

**Source →** [github.com](https://github.com/SmonSE/GhostBLE)

### ELRO Hubs Send Real-Time Events to Home Assistant

Alarm sounds and sensor changes need not stay inside an ELRO Connects system. This custom Home Assistant integration reads K1 and K2 hubs directly, bringing immediate events, battery levels, signal strength, and device states into local automations. The two hub generations use different communication software, so hardware identification matters.

**Source →** [github.com](https://github.com/dib0/ha-elro-connects-realtime)

### Bring TP-Link and Mercusys Routers into Home Assistant

A custom Home Assistant component puts supported TP-Link and Mercusys router data beside your lights and sensors. Installed through HACS, it adds status sensors and controls, but polling runs about every 30 seconds, firmware changes can break compatibility, and router administration may be logged out while the integration is active.

**Source →** [github.com](https://github.com/AlexandrErohin/home-assistant-tplink-router)

### How a $20 ESP8266 Calls and Tracks Elevators

A roughly $20 ESP8266 setup calls an apartment elevator before anyone reaches the hallway, then tracks its movement locally. A relay copies the existing hall-button press, while MQTT, Home Assistant, a permitted camera view, and a door-side display work together without touching the elevator controller.

**Source →** [github.com](https://github.com/europaprof/call14)

### A Self-Hosted UniFi Network Companion

Busy UniFi networks can be difficult to troubleshoot from one dashboard. Network Optimizer offers a self-hosted application with Docker and Windows options, but its repository still needs careful review before deployment. Check its controller access, collected readings, configuration behavior, and supported UniFi versions before trusting it with a live network.

**Source →** [github.com](https://github.com/Ozark-Connect/NetworkOptimizer)

### Anthbot Mowers in Home Assistant—An Unmaintained Integration

Anthbot Genie 600, M5, and M9 mowers can appear in Home Assistant through account lookup, AWS IoT shadow requests, and model-aware sensors. This community integration is no longer maintained, so use it mainly as a technical reference and start with ha-anthbot-map-v2 for a current setup.

**Source →** [github.com](https://github.com/vincentjanv/anthbot_genie_ha)

## Raspberry Pi

### USB SSD Boot or PXE Network Boot?

SD cards can fail in Raspberry Pi projects that run continuously. A USB SSD offers the simplest replacement, while NVMe suits Pi 5 builds that need speed. PXE boot serves several boards from one network server, but it takes more setup and dependable wired networking.

**Source →** [raspberry.tips](https://raspberry.tips/en/raspberrypi-tutorials/raspberry-pi-boot-without-sd-card)

### Build a Portable Offline Internet with a Raspberry Pi

A Raspberry Pi can become a small information hub for places where internet access is weak or absent. This project brings local maps, a Wikipedia copy, and AI tools together over a private connection, while showing the real compromises involving storage, battery life, processing speed, and portability.

**Source →** [the-diy-life.com](https://the-diy-life.com/i-built-a-portable-offline-internet-with-maps-wikipedia-and-local-ai/)

### Build a Raspberry Pi Modbus Logger with Ansible

Several remote environmental loggers can share one design: LibrePiLogger connects Raspberry Pis to Modbus sensors over RS-485, records timestamped CSV data, and uses Ansible for setup. Makers can choose a low-power Pi Zero or faster Pi 4, then add sensor drivers without rewriting the whole logging system.

**Source →** [sciencedirect.com](https://www.sciencedirect.com/science/article/pii/S246806722600074X)

## Robotics

### Building Nexara: An Air-Gapped AI Avatar Head

A pair of round displays, a spatial camera, and a three-axis servo neck give Nexara a physical way to show local AI activity. An ESP32-S3 links those parts while separated power rails protect sensitive electronics from servo noise, keeping the proposed system independent of cloud services.

**Source →** [pcbway.com](https://www.pcbway.com/project/sponsor/Nexara_Edge_AI_Animatronic_Physical_Avatar_Head_5c94782b.html)

---

Full issue: https://www.tinkernews.com/issues/37-build-smarter-repair-deeper · Subscribe: https://www.tinkernews.com
