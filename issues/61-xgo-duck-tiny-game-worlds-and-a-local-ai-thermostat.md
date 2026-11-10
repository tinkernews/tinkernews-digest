# TinkerNews #61: XGO Duck, Tiny Game Worlds, and a Local AI Thermostat

Issue 61 explores practical edge-computing builds: control an XGO Duck from a browser, run neural game worlds on a Pico 2 W, and let an Arduino UNO Q manage a local AI…

*Issue #61 · 2026-11-09*

## Robotics

### Browser-Controlled XGO Duck on Arduino Uno Q

A browser becomes the control panel for an XGO Duck running on Arduino Uno Q. This runtime combines learned ONNX motion policies with Python control and STM32 feedback loops. It handles calibration, recovery, skating, servo safety, and practical diagnostics for makers working with compatible hardware.

**Source →** [github.com](https://github.com/LuwuDynamics/xgoduck_runtime_arduino)

### $1.50 FOC Board Builds a Tiny 10:1 Robot Joint

A 1503 brushless gimbal motor, a roughly $1.50 four-layer FOC board, and a printed 10:1 gearbox make a compact robot joint. The design is open hardware, though its firmware remains open loop and needs configuration work before it can serve as a dependable servo.

**Source →** [github.com](https://github.com/yzytz17/1.5-joint-module)

### MOSS: An Open-Source Litter-Picking Rover

MOSS is a tracked, 3D-printed rover that follows a person and collects small litter with a robotic arm. Its current prototype can drive and demonstrate pick-and-drop handling under teleoperation. Open hardware files, several computer choices, and simulation tools make it a practical project for experienced robotics makers.

**Source →** [github.com](https://github.com/metrox-eth/moss)

## Arduino

### Connect the UNO Q’s Linux and STM32 Sides

A potentiometer on A5 sets the UNO Q’s built-in LED brightness through messages between Python on Debian Linux and an STM32 sketch. This build shows how the Bridge moves data, when to use call() or notify(), why provide_safe() matters, and how a WebSocket page can add browser control.

**Source →** [mischianti.org](https://mischianti.org/arduino-uno-q-bridge-how-python-and-the-stm32-sketch-talk-call-notify-provide/)

### An Arduino UNO Q Runs a Local AI Thermostat

An Arduino UNO Q runs a small language model locally, reads a simulated temperature, and controls an LED fan. Python gives the model limited tools, while the STM32 keeps deterministic control of the hardware. The build also measures startup delay, response speed, memory use, and model size.

**Source →** [mischianti.org](https://mischianti.org/arduino-uno-q-a-local-ai-agent-that-drives-the-hardware/)

## DIY Electronics

### A Mecha Desk Buddy with Drawers and a Touchscreen Face

Thirty-three printed parts form a small mecha organizer with storage for a phone, pens, SD cards, and circuit boards. An ESP32-S3 drives its 2.8-inch touchscreen, while Arduino and LVGL 9 provide blinking eyes and six expressions. The result combines useful desk storage with a friendly animated interface.

**Source →** [hackaday.io](https://hackaday.io/project/207317-yakroo108-mecha-desk-buddy)

## ESP32

### Marelleo: An ESP32 Story Box for NFC Figurines

Marelleo turns an NFC-tagged figurine into a story, song, or radio control. An ESP32 handles detection, Wi-Fi, audio playback, and updates inside a child-ready box. The build moved from breadboard to perfboard and custom PCB, with battery safety, mechanical failures, and recovery testing shaping each revision.

**Source →** [zebra.rodeo](https://zebra.rodeo/en/blog/marelleo/)

### Kube32 Brings kubectl to ESP32 Clusters

Use kubectl to place WebAssembly apps on a small ESP32-S3 cluster. Kube32 pairs a PSRAM-equipped control plane with worker boards such as the M5Stack Cardputer, then treats displays, sensors, storage, and input devices as managed resources. A simulator and practical examples make the setup easier to try.

**Source →** [github.com](https://github.com/arterialist/kube32)

### Build a Browser-Controlled ESP8266 Relay

A NodeMCU ESP8266 can serve a small control page over 2.4 GHz Wi-Fi and switch a relay from any browser on the same network. The project uses one relay, one status LED, and a short Arduino sketch, with clear limits around security, local access, and mains wiring.

**Source →** [anilestore.com](https://anilestore.com/blog/nodemcu-esp8266-wifi-relay-switch)

### ESP32-S3 Rotary Universal Timer

Four timer scales, a rotary encoder, and a circular display give this CrowPanel project a simple way to set and watch time pass. An external buzzer adds three audible alerts at zero, while framebuffer drawing keeps the display smooth. Arduino users need specific ESP32 and graphics library settings.

**Source →** [hackaday.io](https://hackaday.io/project/207144-diy-esp32-universal-timer-with-touchscreen)

### Inside an Open ESP32-S3 Board Designed in KiCad

Built around Espressif's ESP32-S3-WROOM-1-N8R8, this open board packages the schematic, PCB layout, custom KiCad libraries, BOM, Gerbers, drill files, and documentation in one repository. The design is ready for inspection and fabrication, while board assembly, testing, bring-up, and firmware work remain future steps.

**Source →** [github.com](https://github.com/AMIFEX-IT/ESP32-S3-SMALL)

## IoT

### Build a 3D Home Assistant Dashboard

Home Assistant usually shows devices in cards and lists. NeonPlan 3D puts them inside a model of your home, where rooms, lights, blinds, cameras, sensors, energy equipment, and warnings appear in place. You draw or import the plan, link areas, then publish reusable views for dashboards and wall tablets.

**Source →** [github.com](https://github.com/Mastershort/neonplan3d)

### Repurpose an Old Echo for Home Assistant

An old Echo can keep its far-field microphones and local wake-word hardware while dropping Alexa's cloud connection. hassmic routes speech through Home Assistant Assist, with several Echos choosing one responder locally. It also supports local music, Bluetooth, automations, and Show displays, though installation involves firmware work and real brick risk.

**Source →** [github.com](https://github.com/Gamer92000/echo-dot-assist)

### Build a Live 3D Smart-Home Controller

House Control turns a JSON floor plan into a live 3D control surface for lights, air conditioners, scenes, and sensors. Native Mac and iPhone apps connect Smart Life, Home Assistant, Philips Hue, and Apple Home, while simulated devices, local storage, and HTTP or MCP access keep experimentation practical.

**Source →** [github.com](https://github.com/0xProbabillity/house-control)

### Marstek Venus E Meets Home Assistant

A LilyGO T-CAN485 reads a Marstek Venus E over RS485 and sends local battery data to Home Assistant through ESPHome. The build adds energy history, warnings, runtime estimates, and operating controls, while keeping the battery connection, firmware version, secrets, and ESP32 hardware limits in view.

**Source →** [github.com](https://github.com/whyisthisbroken/marstek-lilygo-rs485)

### ESP8266 Wi-Fi Bridge for Pylontech Batteries

PylontechMonitoring connects a battery stack’s RS-232 console to a Wemos D1 Mini through a MAX3232 transceiver. The ESP8266 sends battery and module readings to MQTT, where Home Assistant can create sensors automatically. A browser console, JSON endpoint, and wireless firmware updates support maintenance and custom dashboards.

**Source →** [github.com](https://github.com/hidaba/PylontechMonitoring)

### SpiderBridge Puts GGS Control on Home Assistant

A roughly €10 ESP32 can sit between a Spider Farmer GGS controller and Home Assistant, keeping control on your network. SpiderBridge installs through a browser, provisions the controller over Bluetooth once, then handles Wi-Fi, TLS, MQTT, cloud forwarding, and local automation without a Raspberry Pi.

**Source →** [github.com](https://github.com/matthias1232/spider-farmer-homeassistant)

### Turn a Cheap Wi-Fi Clock Into an ESP32 Display

A closed-firmware HU-058D clock becomes a Home Assistant display when an ESP32-WROOM-32 takes over its RGB panel. The build keeps the case and LEDs, adds custom effects and controls, and can expose temperature, light, and buzzer hardware, depending on the firmware configuration and board variant.

**Source →** [github.com](https://github.com/dpavlin/HU-058_ESPHome-NTC-LDR-Buzzer)

## Raspberry Pi

### A Pico 2 W Runs Its Own Tiny Game Worlds

Five small games run on a Raspberry Pi Pico 2 W while two neural networks generate frames and choose actions. The project combines grid tokens, a reused transformer block, int8 weights, game-aware decoding, and dual-core scheduling. Results are strong on simple games, though Pac-Man and Doom-lite still expose clear limits.

**Source →** [github.com](https://github.com/SheepSeb/tinyworldformer)

### A Raspberry Pi 5 Knowledge Box for Offline Use

A Raspberry Pi 5, NVMe SSD, and local Wi-Fi network can carry Wikipedia, maps, medical references, repair guides, and emergency material without internet access. HAS_PrepperDisk adds Internet-in-a-Box, Kiwix, automated downloads, a browser homepage, and health checks for use in remote or disrupted settings.

**Source →** [github.com](https://github.com/schematrix/HAS_Prepper_Disk)

### Raspberry Pi CRT Tracks Spacecraft in Retro Mission Console

A Raspberry Pi drives a 640x480 mission-control display on a composite CRT, while Rust gathers spacecraft positions, telemetry, schedules, and sky data. mctl offers interactive pages, unattended kiosk scenes, offline caching, replay, and several period-style themes. A Pi 3B+ handles it through software rendering at modest frame rates.

**Source →** [github.com](https://github.com/LiamDroog/mctl)

### Build a Raspberry Pi Marine Radar Display

At the navigation station, a Raspberry Pi combines Raymarine Quantum radar data with Signal K readings, AIS contacts, and anchor monitoring. Exodus Radar renders the view on an HDMI screen or browser, while Python services handle decoding and control. It remains a Quantum-specific, experimental aid, not certified navigation equipment.

**Source →** [github.com](https://github.com/sailingexodus/exodus-radar)

### Build an RFID Reader for Raspberry Pi 5

Older RC522 tutorials often fail on Raspberry Pi 5 because they depend on RPi.GPIO. This build uses SPI through spidev and reset control through gpiod. Wire the reader at 3.3 V, read card UIDs, then use those values for a hobby access project. UID matching suits demonstrations, not high-security systems.

**Source →** [raspberry.tips](https://raspberry.tips/en/raspberrypi-einsteiger/raspberry-pi-5-rfid-rc522-guide)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-61)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-61)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-61)

## From the bench

### Voltage divider calculator

One of 19 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools?utm_source=issue_page&utm_medium=bench&utm_campaign=issue-61)

---

Full issue: https://www.tinkernews.com/issues/61-xgo-duck-tiny-game-worlds-and-a-local-ai-thermostat · Subscribe: https://www.tinkernews.com
