# TinkerNews #58: MatTris, MirrorBallBot, and the ESP32 Science Tricorder

Issue 58 brings hands-on builds spanning a pocket Arduino arcade, a Raspberry Pi robot balancing on a ball, and an open-source ESP32 science tricorder—plus practical projects for…

*Issue #58 · 2026-10-19*

## IoT

### Build an ESP32 SHT41 Temperature and Humidity Monitor

An ESP32 and SHT41 form a compact environmental monitor with simple four wire I2C connections. The Arduino IDE can send readings to the Serial Monitor or an OLED. With factory calibration, useful accuracy, low power needs, and SHT4x compatibility, this build provides a practical base for larger IoT projects.

**Source →** [randomnerdtutorials.com](https://randomnerdtutorials.com/esp32-sht41-temperature-humidity-arduino/)

### This ESP32 Bin Tracks Fill Levels and Collection Routes

Fixed collection schedules send crews to bins that may be empty while busy locations overflow. This project uses an HC-SR04, ESP32, Wi-Fi, MQTT, and a dashboard to measure fill levels, report alerts, and suggest collection routes. It offers a clear, practical IoT example for campuses, canteens, and municipal services.

**Source →** [projectech.in](https://projectech.in/projects/smart-dustbin-fill-level-esp32-dashboard/)

### ESPHome Bridge Reads JK-BMS Data

Battery packs often contain useful data that stays trapped inside the BMS. This ESPHome component places an ESP32 between a JK-BMS and Home Assistant, using UART-TTL or BLE to decode pack and cell readings. It adds dashboards, alerts, and automations without replacing the battery system’s safety functions.

**Source →** [github.com](https://github.com/syssi/esphome-jk-bms)

### Build a Wi-Fi to Ethernet ESP32 Router

An ESP32 with a W5500 Ethernet interface can share an existing Wi-Fi connection with wired devices. This project provides a separate LAN, DHCP, NAT, routed mode, and optional WireGuard protection. It suits home labs, isolated IoT testing, and devices that cannot join enterprise Wi-Fi directly.

**Source →** [github.com](https://github.com/martin-ger/esp32_ethernet_router)

### Turning a CYD into a Wireless Security Toolkit

A $7 ESP32 Cheap Yellow Display can become a handheld wireless security tester with HaleHound CYD firmware. Its touchscreen groups more than 40 modules in one interface, while browser flashing keeps setup simple. Some functions need extra radios, so check the hardware notes before building and testing in an authorized lab.

**Source →** [github.com](https://github.com/JesseCHale/HaleHound-CYD)

### Building an ESP32 Audio Bridge for Beolab Speakers

Vintage Beolab speakers need a quieter signal than a PCM5102A normally provides. This ESP32-S3 bridge handles TV and network audio with careful attenuation, 32-bit processing, source trims, startup muting, and practical fault finding. Its lessons cover Ethernet timing, PCB footprints, power cleanup, and diagnosing audio task underruns.

**Source →** [hackaday.io](https://hackaday.io/project/206915-radiostreamer-tv-fiberdr-lyd-for-vintage-beolab)

### ESP32 Field Camera Meets Reality

A low-cost camera node can capture images on a workbench, yet field use exposes weak links. This build connects an ESP32-S3, OV5640, Android phone, Flutter app, and cloud AI, then examines communication, image quality, app boundaries, and code maintenance.

**Source →** [note.com](https://note.com/kisspan/n/n78bc9e25bc20?hl=en)

## 3D Printing

### M3-CRETE: A Meter Scale Paste Printing Reference

M3-CRETE gives qualified teams a documented starting point for meter scale cementitious paste printing. It covers mechanical design, low voltage interfaces, configuration, and BOM information, while leaving high risk electrical work, material validation, safety engineering, and construction compliance to each builder and their own controlled facility.

**Source →** [github.com](https://github.com/sunnyday-technologies/M3-CRETE)

## Arduino

### Self Contained PIR Trigger for Halloween Props

A small 9V module gives Halloween animatronics a portable motion trigger. An HC-SR501 senses movement, while a PC817 optocoupler separates that sensor circuit from the prop control wiring. A custom two part enclosure protects the electronics, holds the battery hardware, and keeps the assembly easy to place.

**Source →** [blog.adafruit.com](https://blog.adafruit.com/2026/10/15/motion-sensor-for-halloween-animatronics-hc-sr501-pir-pc817-optocoupler-enclosure-3dthursday-3dprinting/)

### Pocket Tetris Arcade with Arduino and LED Matrix

A familiar block game becomes a real tabletop object in MatTris Arcade. An Arduino-compatible controller runs the game, an LED matrix shows the playfield, and physical buttons handle play. The 21-step build follows the enclosure, wiring, assembly, programming, and testing needed to make the console feel complete.

**Source →** [instructables.com](https://www.instructables.com/MatTris-Arcade/)

## DIY Electronics

### Build a Knock Activated Monster Box

A tiny knock becomes a surprisingly expressive Halloween reaction. This child friendly box uses an electret microphone, a one transistor amplifier, an Arduino, and a servo to sense sound and move a monster. Its schematic and construction notes also teach biasing, AC coupling, threshold detection, and servo control through one playful build.

**Source →** [build-electronic-circuits.com](https://www.build-electronic-circuits.com/mini-monster-box-halloween-project/)

### OnePage: Build an ESP32 C61 E Reader

OnePage turns an ESP32 C61 board into the center of a complete DIY e reader project. Its repository connects electronics, firmware, enclosure files, a board SDK, and browser tools, giving makers a practical way to inspect, source, fabricate, assemble, and adapt a wireless handheld reading device.

**Source →** [github.com](https://github.com/MoveCall/onepage-reader)

### Building a PYNQ-Z2 Mixed-Signal Oscilloscope

A custom PCB turns the PYNQ-Z2 into an open measurement platform with a dual channel, 16 bit oscilloscope, logic analyzer connection, and arbitrary waveform generator. FPGA logic handles acquisition and processing, while ngscopeclient provides a desktop view. The repository also documents planned AI integration, though implementation details remain limited.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/PYNQ_Z2_Mixed_Signal_Oscilloscope_FPGA_Based_Open_Instrumentation_AI_Integra_d2309cab.html)

### RP1 Opens the Full Humanoid Robot Stack

RP1 treats a humanoid robot as a reproducible system, not a sealed demonstration. Its repository connects structure, joints, electronics, firmware, control, and learning tools, while publishing CAD, schematics, PCB layouts, Gerbers, BOM data, and assembly notes for builders with serious fabrication and robotics experience.

**Source →** [github.com](https://github.com/Roboparty/RP1)

### OnePage: Build an ESP32 C61 E Reader

OnePage turns an ESP32 C61 board into the center of a complete DIY e reader project. Its repository connects electronics, firmware, enclosure files, a board SDK, and browser tools, giving makers a practical way to inspect, source, fabricate, assemble, and adapt a wireless handheld reading device.

**Source →** [github.com](https://github.com/MoveCall/onepage-reader)

## ESP32

### Give an Arduino Wired Ethernet with ENC28J60

Getting a low-cost ENC28J60 board working with an Arduino Nano takes more than connecting an Ethernet cable. SPI wiring, chip-select settings, library choice, and voltage checks all matter. Once configured, the small controller can join a LAN for web pages or data exchange, though ESP32 users need different pins and software.

**Source →** [tweaking4all.com](https://www.tweaking4all.com/hardware/arduino/arduino-enc28j60-ethernet/)

### Build 16 Expandable GPIO Channels for ESP32

Running short on ESP32 pins is common when a project adds relays, buttons, sensors, and indicators. This compact MCP23017 board moves those signals onto I²C, provides 16 terminal connections, and supports eight addressable modules. Reverse polarity protection, 5 V regulation, and clear address LEDs keep the hardware practical.

**Source →** [elektormagazine.com](https://www.elektormagazine.com/labs/basic-gpio-expander-mcp23017-4)

### Connect a Zehnder ComfoAir Q to Home Assistant

An ESP32 and CAN transceiver give a Zehnder ComfoAir Q a practical link to Home Assistant. This ESPHome project carries ventilation data and airflow commands from the unit’s CAN bus to the ESPHome API, with board choices, wiring guides, power notes, and OTA updates included.

**Source →** [github.com](https://github.com/yoziru/esphome-zehnder-comfoair)

### Building an Open Source ESP32 Science Tricorder

This handheld cyberdeck packs an ESP32, custom sensor boards, a microspectrometer, a magnetometer, and a Python interface into a 3D printed enclosure. Its open repository includes firmware, PCB layouts, print files, assembly guidance, and design history, giving makers a practical reference for building portable scientific instruments.

**Source →** [github.com](https://github.com/tricorderproject/cyberdeck)

## Raspberry Pi

### 13 Games on a $5 Raspberry Pi Pico 2

A breadboard, a small color display, physical switches, and a speaker turn a roughly $5 Raspberry Pi Pico 2 into a playable 13 game arcade. Pico2Arcade uses the RP2350 to handle graphics, controls, sound, and game timing at a claimed 60 frames per second. Its open source code and build notes are on GitHub.

**Source →** [icode.com](https://www.icode.com/pico2arcade-13-classic-arcade-games-on-a-5-raspberry-pi-pico-2-now-open-source/)

### A Raspberry Pi Robot That Balances on a Ball

MirrorBallBot replaces wheels with one spherical contact point, using motorized rollers to keep its body upright and moving. A custom Raspberry Pi HAT connects the electronics, while camera feedback and Python software guide corrections. Demonstrations include finger following, disturbance recovery, and travel along predefined paths.

**Source →** [instructables.com](https://www.instructables.com/MirrorBallBot-MBB-an-Alternative-Ball-Balancing-Ro)

### Run a Local AI Assistant on Raspberry Pi

ZeroClaw provides a Rust-based, self-hosted agent runtime for Raspberry Pi projects. It can connect natural-language requests with software tools and interfaces such as GPIO, I2C, SPI, and USB. This is a software foundation, not a finished robot, so wiring, model setup, permissions, and safety rules remain your responsibility.

**Source →** [github.com](https://github.com/zeroclaw-labs/zeroclaw)

## Robotics

### Build a PID Line Following Robot

At the front of this small robot, several IR sensors read the floor while two motors make constant steering corrections. The project links sensing, position estimates, feedback code, motor control, calibration, and mechanical design in one machine that immediately shows whether each part is working.

**Source →** [gra.ge](https://gra.ge/blogs/20)

### Arduino PT100 and PT1000 PID Controller PCB

Stable temperature control starts with good feedback. TSRCT-PCB-01 pairs an Arduino Nano Every with PT100 and PT1000 inputs, PID firmware, and two 5 V SSR outputs. The KiCad board provides a practical base for experimental heaters, while details such as calibration, display hardware, and temperature range need confirmation.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/TSRCT_PT100_PT1000_SSR_PID_Temperature_Controller_0d5c73a0.html)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-58)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-58)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-58)

## From the bench

### Voltage drop and wire gauge

One of 15 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools?utm_source=issue_page&utm_medium=bench&utm_campaign=issue-58)

---

Full issue: https://www.tinkernews.com/issues/58-mattris-mirrorballbot-and-the-esp32-science-tricorder · Subscribe: https://www.tinkernews.com
