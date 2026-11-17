# TinkerNews #62: Tiny BASIC, an ESP32 PC XT, and a Trash Collecting Robot

This issue has an Arduino that runs BASIC, an ESP32 that recreates an IBM PC XT, a robot that finds and collects trash, a Raspberry Pi security key, e paper displays, LoRa…

*Issue #62 · 2026-11-16*

## DIY Electronics

### Build a $10-Class RISC-V Handheld Game Console

A coin-cell handheld built around a roughly ten-cent RISC-V chip runs a surprisingly large set of games on a tiny monochrome screen. This project combines a custom PCB, simple controls, 3D-printed case, low-power audio, and several firmware options, while showing where battery life and programming hardware set limits.

**Source →** [github.com](https://github.com/wagiminator/CH32V003-GameConsole)

### Making a Low-Power Bike Computer

A bike computer needs more than speed and a map when it must save power, respond quickly, and stay readable outdoors. This ESP32-S3 prototype uses damage-based rendering, simplified vector maps, cached tiles, and careful memory management. Its biggest lesson is that efficient pixels and short wake times matter as much as processor speed.

**Source →** [marvinh.dev](https://marvinh.dev/blog/bike-computer/)

### Give an Amstrad PCW Wi-Fi with PerryFi 2

PerryFi 2 gives an Amstrad PCW Wi-Fi through its original expansion interface. A Raspberry Pi Pico handles the PCW-facing serial hardware, while an ESP-12F provides modem-style commands, SLIP, and PPP networking. Builders can choose direct mounting or Backplane use, then flash separate firmware and boot the correct disk image for their PCW.

**Source →** [github.com](https://github.com/SanPollo/PerryFi2)

## 3D Printing

### Turning an Ender-3 into a PicoEMP Rig

A stock Ender-3 V3 SE can position a PicoEMP probe over a chip for repeatable EMFI tests. A printed mount, indexed target holder, USB serial control, and Python wrappers turn manual probing into logged coordinate sweeps, while mechanical error and high-voltage safety remain important limits.

**Source →** [anvilsecure.com](https://www.anvilsecure.com/blog/picoemp-3d-printer-fault-injection-rig.html)

### Bambu Bar Puts Printer Status in Your Menu Bar

A small desktop utility keeps Bambu Lab printer status close at hand. Bambu Bar reads progress, temperatures, filament, errors, and camera views over the local network, then shows them in a menu bar or system tray. It also handles several printers and offers limited controls when the printer permits them.

**Source →** [github.com](https://github.com/rolottr/bambu-bar)

## Arduino

### Run BASIC Directly on an Arduino

Tiny Basic turns a mid-range Arduino into a small, self-contained BASIC computer. You can write, edit, and run programs on the board through its in-hardware editor, without returning to a PC IDE for every change. Its library also covers hardware I/O, math, and bit manipulation for hands-on experiments.

**Source →** [dilshan.github.io](https://dilshan.github.io/tiny-basic/)

### Arduino scanner for 1991-95 Jeep computers

A $3 Arduino Nano bridges a 1991-95 Jeep engine computer to a laptop. This project combines measured connector wiring, SCI protocol code, a Python scanner, and guided setup instructions. It reads fault codes, shows live data, records drives, and runs tests, with careful meter checks required before power is connected.

**Source →** [github.com](https://github.com/MZULALI/xj-scanner)

### ExcaliPad: USB-C Keyboard and Game Controller

ExcaliPad puts tactile buttons and a two-axis thumb joystick on one Arduino-compatible PCB. An ATmega32U4 handles native USB, letting the board appear as a keyboard, gamepad, or custom HID device. Its firmware can support games, macros, mouse control, accessibility tools, and application-specific input panels.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/ExcaliPad_A_USB_C_Keyboard_and_Game_Controller_Board_with_a_Thumb_Joystick_3d2ca8a9.html)

## ESP32

### This ESP32 Runs a Complete IBM PC/XT

One ESP32 recreates an early IBM PC on a postcard-sized board, complete with VGA, PS/2 ports, microSD storage, audio and DOS support. The design splits video timing and 8086 emulation between the chip's cores, making it a useful study in retrocomputing, real-time firmware and compact PCB design.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/ESP32_x86_PC_A_Complete_IBM_PC_XT_Compatible_Computer_on_a_Single_Board_4eb2b002.html)

### ESP32 Arcade Matrix With HUB75 Panels

An ESP32 drives a HUB75 RGB matrix as an arcade clock, marquee, dashboard, or retro media screen. ArcadeMatrix stores settings and media on a MicroSD card, while Wi-Fi connects weather, MQTT, Home Assistant, and other services. ESP32-S3 boards add larger panels and more demanding graphics.

**Source →** [github.com](https://github.com/red77290/ArcadeMatrix)

### One ESP32 Firmware Base for Many E-Paper Displays

More than one display family can share a single ESP-IDF firmware base here. The device wakes, connects to Wi-Fi, fetches a panel-ready frame from Tesserae, refreshes the screen, reports status, and sleeps. A shared driver interface keeps board support, provisioning, and power handling in one place.

**Source →** [github.com](https://github.com/dmellok/tesserae-device-firmware)

### ESP32 Gadgets Get Host-Controlled Dashboard Widgets

Hermes Gadget SDK connects ESP32 voice gadgets to a Linux host that can publish small dashboard pages. The new widgets show values, progress, lists, or headlines, then fit beside the idle clock. Gestures, fallback tiles, storage locks, limits, expiration, and voice interruptions make the feature practical for daily status displays.

**Source →** [github.com](https://github.com/Adolanium/hermes-gadget-sdk)

## IoT

### Hands-On LoRa Link with Two Arduino Unos

Two Arduino Unos trade numbered hello packets through SX1278 radios in a browser simulation. You can inspect the wiring, Arduino LoRa sketches, packet airtime, RSSI, and signal changes as the radios move apart, then test mismatched settings before buying modules for a physical point-to-point sensor link.

**Source →** [mokxi.com](https://mokxi.com/lora-simulator)

### Building a Solar LoRaWAN Sensor Node

The Green Dot Board combines solar and LiPo power, an RP2040 controller, LoRaWAN connectivity, and sensor ports for agricultural monitoring. Its MicroPython firmware reads temperature and humidity, packs the values for transmission, and sends them through a LoRa-E5 to a Loriot dashboard, while RS485 support covers longer cable runs.

**Source →** [flux.ai](https://www.flux.ai/p/blog/how-to-design-and-deploy-a-lora-iot-sensor-node-with-rp2040)

### Build a Local ESP32 Gateway for Wallbox Control

A roughly $15 ESP32 board can control a Wallbox Pulsar charger over BLE without relying on Wallbox servers. It connects to MQTT and Home Assistant, records real charging sessions, hosts a local dashboard, and supports OTA updates. The build needs USB power, BLE range, and careful security settings.

**Source →** [github.com](https://github.com/botts7/esp32-wallbox)

### Smart Home Devices That Work Offline

Cloud access can disappear while a light, sensor, or switch still needs to work. This local-first design uses ESP8266 or ESP32 devices, Tasmota firmware, MQTT, and local automation logic. Internet access remains useful for remote control and notifications, while everyday actions stay on the home network.

**Source →** [coderlegion.com](https://coderlegion.com/34362/why-smart-home-devices-should-work-without-the-internet-and-how-to-design-one-that-does)

## Raspberry Pi

### TelltaleDNS: A Raspberry Pi DNS Server With Per-Device Rules

DNS requests become much easier to inspect when TelltaleDNS runs between home devices and the wider internet. The Rust service logs queries, applies rules by device or group, explains decisions, and forwards allowed requests to chosen upstreams. It can run on a Raspberry Pi and grow into a clustered setup.

**Source →** [github.com](https://github.com/paimonsoror/telltaledns)

### RS-Key: A Raspberry Pi Security Key

RS-Key turns a Raspberry Pi RP2350 into a security key for passkeys, SSH, Git signing, smart-card applications, and one-time passwords. Its Rust firmware handles several protocols, while the touchscreen version keeps PIN entry and approval on the device. The repository also documents testing, board differences, and fault handling.

**Source →** [github.com](https://github.com/TheMaxMur/RS-Key)

### Pico 2 W Recovery for the M-VAVE FM-1

A Raspberry Pi Pico 2 W gives the M-VAVE FM-1 a controlled path into its mask-ROM bootloader. The project compares fresh firmware dumps, limits writes to the application area, and reads sectors back afterward. Stock V15 recovery works, while installing Lunar firmware on FM-1 hardware remains unproven.

**Source →** [github.com](https://github.com/ip2k/lunar-modulator)

## Robotics

### Four-Servo Arm Control in a Browser

Four SG90 servos, two thumb joysticks, and an Arduino Uno make this browser simulation a useful test bench for robot-arm code. It shows rate-based joint control, angle limits, dead-band handling, serial feedback, and the gap between a safe software model and real servo power, collisions, and load handling.

**Source →** [mokxi.com](https://mokxi.com/robot-arm-simulator)

### A Simulated MeArm Robot Plays Connect Four

A simulated MeArm plays Connect Four against a person while PyBullet handles gravity, collisions, and arm movement. Python separates the game window from the physics process, while Minimax chooses the robot's moves. Calibration data, safe movement steps, and tuned token physics keep the virtual arm from hitting the board.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/MeArm_Connect4_Simulation_6f6be9d6.html)

### A Webcam-Guided MeArm Sorts Colored Balls

Colored balls become simple targets for this printed MeArm robot. A webcam finds each ball, Python maps its position to millimeters, and an Arduino moves four SG90 servos through a calibrated pickup path. The design also shows how fixed motion limits can make inexpensive hardware behave more reliably.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/MeArm_PickPlace_d0e5d76e.html)

### How This Robot Finds and Collects Trash

A Traxxas-based robot spots a target, steers toward it, stops about 0.16 meters away, and hands the pickup to an SO101 arm. Its OAK-D Lite handles detection while an LD19 LiDAR handles stopping distance, giving a Raspberry Pi 5 a simple control job on real hardware.

**Source →** [marcusgreenan.com](https://marcusgreenan.com/documents/mae148-report.pdf)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-62)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-62)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-62)

## From the bench

### ESP32 DevKit V1 pinout

One of 19 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools)

---

Full issue: https://www.tinkernews.com/issues/62-tiny-basic-an-esp32-pc-xt-and-a-trash-collecting-robot · Subscribe: https://www.tinkernews.com
