# TinkerNews #54: Practical Builds for Smarter Spaces

Build an all-sky camera, energy dashboard, Wi-Fi sensor, touchscreen music panel, workshop tester, quadruped robot, and more with Raspberry Pi, ESP32, 3D printing, and…

*Issue #54 · 2026-09-21*

## ESP32

### Build an ESP32 MAX30102 Vital Signs Sensor

Three useful readings come from one fingertip module: heart rate, SpO2, and temperature. This ESP32 project covers the wiring, Arduino sketches, and optical sensing behind each value. It is a practical introduction to I2C and physiological data, but the results are experimental and not suitable for medical diagnosis.

**Source →** [randomnerdtutorials.com](https://randomnerdtutorials.com/esp32-max30102-oximeter-heart-rate-sensor/)

### Build an ESP32 Cooker Whistle Counter

Pressure-cooker whistles are easy to miss when the kitchen gets busy. This ESP32 project uses a MAX4466 microphone to count sound events, then sends a WhatsApp message through CircuitDigest Cloud when the selected count is reached. It needs careful calibration, reliable Wi-Fi, and continued supervision around the cooker.

**Source →** [circuitdigest.com](https://circuitdigest.com/microcontroller-projects/smart-cooker-whistle-counter-using-esp32)

### ESP32 Touchscreen Sonos Wall Panel

On a desk or wall, SonosESP turns a 4-inch or 7-inch touchscreen and ESP32-P4 into a dedicated music remote. It browses libraries, controls speakers across rooms, shows album art and lyrics, displays weather and clocks, and receives firmware updates without being removed from its mounting.

**Source →** [github.com](https://github.com/OpenSurface/SonosESP)

### ESP32 Tesla BLE Control with Home Assistant

Turn an ESP32 into a local Tesla BLE bridge with ESPHome and Home Assistant. This project brings charging controls, vehicle data, and diagnostics into a dashboard, while keeping communication nearby. Start with the tested YAML example, check pairing and range, and protect every command that can affect the car.

**Source →** [github.com](https://github.com/PedroKTFC/esphome-tesla-ble)

### Replace a RIKA Stove Dongle with ESP32-S3

RIKA pellet stoves normally send data through a proprietary Firenet 2.0 dongle and cloud service. Open Firenet substitutes an ESP32-S3, speaking the stove’s USB protocol while providing Wi-Fi, a local control page, and a REST API. Careful board selection matters, and this unofficial appliance interface carries real installation risks.

**Source →** [github.com](https://github.com/openfirenet/open-firenet)

### RuView: WiFi Sensing Through Walls

Ordinary WiFi signals become motion clues in RuView, a project built around ESP32 sensing nodes, local processing, live displays, and home-automation links. It estimates presence, movement, breathing, and heart rate without cameras, but room layout, calibration, interference, and privacy determine how useful those results are.

**Source →** [github.com](https://github.com/ruvnet/RuView?ref=genaisecretsauce.com)

## 3D Printing

### Build an Open-Source RP2040 Logic IC Tester

Bench testing gets a practical companion in the OD-PT74, an open-source RP2040 tester for 14-, 16-, and 20-pin 74xx TTL and CMOS chips. Its OLED, rotary encoder, selectable test modes, complete PCB files, and editable 3D-printed enclosure make it a reproducible workshop instrument.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/OD_PT74_Logic_IC_Tester_bdea1987.html)

### Yertle: A 3D-Printed Quadruped for Locomotion Research

Four printed legs give Yertle a practical robot for studying locomotion. Its open-source files cover the mechanical build, while C++ and Python connect hardware with control, simulation, and machine-learning work. Expect assembly, electronics, programming, and calibration—not a ready-made machine.

**Source →** [github.com](https://github.com/Jerome-Graves/yertle)

## DIY Electronics

### A CYD Project Menu for Makers

One inexpensive ESP32 Cheap Yellow Display can become a music dashboard, F1 notifier, game system, video player, graphics demo, or 3D-printer panel. This community directory gathers links and flashing tools in one place, while reminding readers to check each project’s parts, documentation, wiring, and installation steps first.

**Source →** [github.com](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/blob/main/PROJECTS.md)

## IoT

### Turning an E-Waste PC into a Router

An old Intel board can make a useful router, but this build hit a software snag: OpenWrt booted while its missing e1000e module hid the 82574L ports. The project then tests OPNsense, weighing a lightweight setup against a fuller firewall platform and showing why drivers matter.

**Source →** [hackaday.com](https://hackaday.com/2026/09/21/diy-router-on-x86-e-waste-openwrt-and-opnsense/)

## Raspberry Pi

### Run a Powerwall Grafana Dashboard on a Raspberry Pi

A Raspberry Pi can turn Tesla Powerwall readings into useful history. This open-source build collects battery, solar, household, and grid data, stores it as time-series measurements, and presents it in Grafana. You get a practical view of energy habits without giving the Pi control of the battery.

**Source →** [github.com](https://github.com/jasonacox/Powerwall-Dashboard)

### A Raspberry Pi Repeater Daemon in Python

A Raspberry Pi-class Linux computer can sit at the center of an OpenHop repeater, running a Python daemon that connects communications software to external radio or audio hardware. The repository’s 1,274 commits, 277 stars, and recent restart fix point to a maintained project, though wiring and setup details need verification.

**Source →** [github.com](https://github.com/openhop-dev/openhop_repeater)

### Build an Automated Raspberry Pi All-Sky Camera

A Raspberry Pi can run an unattended all-sky camera, controlling compatible astronomy hardware through INDI and saving repeated frames for later review. This project supplies the software foundation; makers still need the camera, lens, enclosure, power, and storage for reliable night-time monitoring.

**Source →** [github.com](https://github.com/aaronwmorris/indi-allsky)

### Build a Raspberry Pi Homelab Monitor

Running several home-lab machines and Docker services gets difficult when every check lives in a different tab. homelab-monitor offers a local dashboard for host and container health, plus an MCP server for compatible clients. It looks promising on a Raspberry Pi, but installation, hardware, and metric details still need repository verification.

**Source →** [github.com](https://github.com/SikamikanikoBG/homelab-monitor)

## Robotics

### Inside Pistonudo: A Student-Built WRO Robot

Two YouTube runs show Pistonudo tackling WRO Future Engineers 2026, but the ChaBots repository offers more than competition footage. It records the Mexican team’s route from last season’s lessons through mechanics, electronics, software, obstacle handling, testing, serviceability, and cost planning for a working autonomous robot.

**Source →** [github.com](https://github.com/chaBotsMX/chaBots-Tuneados-WRO-Future-Engineers-2026)

---

Full issue: https://www.tinkernews.com/issues/54-practical-builds-for-smarter-spaces · Subscribe: https://www.tinkernews.com
