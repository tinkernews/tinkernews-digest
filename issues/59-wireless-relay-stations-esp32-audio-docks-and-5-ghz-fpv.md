# TinkerNews #59: Wireless Relay Stations, ESP32 Audio Docks, and 5 GHz FPV Video

Issue 59 brings together practical builds including a two-board NRF24L01 relay station, an ESP32 networked audio dock, an ESP32-C5 analog FPV video receiver, and a custom…

*Issue #59 · 2026-10-26*

## Arduino

### Build a Wireless Arduino Relay Control Station

Two Arduino boards share the work in this practical BlueCore build. A Mega serves as the central station, while an Uno collects sensor readings and controls relays at a distance. NRF24L01 radios carry messages both ways, with code, schematics, and wiring diagrams included for reproduction and adaptation.

**Source →** [instructables.com](https://www.instructables.com/BlueCore-Wireless-Sensor-Control-Station-Arduino-M/)

### Build a Wireless Alphabet LED Wall

A familiar TV prop becomes a practical electronics lesson here. This weekend build combines a crafted alphabet panel, a multiplexed LED matrix, an Arduino, and wireless control. The available article excerpt does not name the exact board, wireless module, pins, or command method, so those details need checking before publication.

**Source →** [instructables.com](https://www.instructables.com/Stranger-Things-Alphabet-LED-Wall-Matrix-Multiplex/)

### Simulate Traffic Signals with Arduino and Proteus

A Proteus simulation shows a multi-arm intersection changing lamp states while separate displays count down each phase. One Arduino runs the signal sequence, and a second handles MAX7219 displays through serial data. It is a useful way to test timing, communication, and display behavior before building hardware.

**Source →** [github.com](https://github.com/sprasapradip/proteus-project)

### Building an ESP32 Audio Dock

This project puts an ESP32, network access, physical controls, and dedicated audio hardware into one dock. Its repository brings together electronics files, ESPHome configuration, factory images, and browser installation tools, giving makers a practical starting point for assembling the device and adapting its firmware to related hardware.

**Source →** [github.com](https://github.com/sonocotta/esp32-audio-dock)

### From Schematic to Finished Board: Arduino PCB in KiCad

A blank KiCad project becomes a fabricated Arduino-compatible board through schematic capture, footprint selection, routing, checking, and manufacturing files. The build shows how an ATtiny3226, USB-C power and data, UPDI programming, regulation, headers, and familiar software support can fit into a custom board design.

**Source →** [community.element14.com](https://community.element14.com/challenges-projects/element14-presents/project-videos/w/documents/72057/your-first-real-pcb-in-kicad-an-arduino-compatible-board-designed-from-scratch)

### Move Your Arduino Prototype to a Custom PCB

Loose jumper wires are often the first sign that a working Arduino project needs a better home. This guide compares an Uno shield, a module carrier, and a standalone ATmega328P board, then covers schematic capture, power, programming, layout, and fabrication checks for a reliable custom build.

**Source →** [pcbeditor.com](https://pcbeditor.com/arduino-to-pcb)

### Build an Arduino Ultrasonic Distance Meter

Reflected sound gives an Arduino a simple way to measure distance. This project pairs an HC-SR04-style ultrasonic sensor with basic timing code, wiring, and a calculated reading. It also shows where results can vary, so makers can test calibration before using the circuit in robots, alarms, or level sensors.

**Source →** [researchgate.net](https://www.researchgate.net/publication/367162982_DISTANCE_MEASUREMENT_USING_ULTRASONIC_SENSOR_ARDUINO)

## 3D Printing

### Kiln Connects AI Assistants to 3D Printers

Kiln adds an MCP layer between compatible AI assistants and existing 3D printer services. A maker can connect OctoPrint, Moonraker, PrusaLink, or a USB printer, then inspect status, prepare jobs, start prints, and monitor progress, while keeping approval gates for files, heat, motion, and unattended operation.

**Source →** [github.com](https://github.com/codeofaxel/kiln)

## DIY Electronics

### Build a Simple Milliohmmeter

Ordinary meters often miss the resistance in short wires and joints. This build applies a known current, measures the resulting voltage, and calculates resistance with Ohm’s law. Regulator ICs, a digital voltmeter, and four wire sensing make a useful teaching tool, though accuracy depends on contacts, wiring, resolution, and calibration.

**Source →** [eleccircuit.com](https://www.eleccircuit.com/designing-diy-precision-milli-ohmmeter-circuit/)

### Pico.Lab: Raspberry Pi Pico USB Web Multitool

Cramped benches make full sized test equipment awkward, while many compact instruments cost too much or rely on command lines. Pico.Lab uses an ordinary Raspberry Pi Pico, a USB hosted browser interface, and an analog front end to handle quick checks, while leaving demanding measurements to dedicated lab equipment.

**Source →** [hackaday.io](https://hackaday.io/project/207129-picolab-web-gui-embedded-multitool)

### Build an ESP32-S3 E-Reader Mainboard

Silkscreen provides the electronics for a pocket e-reader without hiding the design from builders. Its ESP32-S3, e-paper connector, battery charging, microSD storage, and physical buttons form a useful starting point. Production files simplify ordering, but Silkscreen firmware is not publicly available yet, so check software status first.

**Source →** [github.com](https://github.com/iandchasse/silkscreen-pcb)

## ESP32

### An ESP32-S3 Board Connects Vending Machines to Cashless Services

Inside a narrow four-layer PCB, an ESP32-S3 links a vending machine’s isolated MDB bus with Wi-Fi, cashless services, telemetry, sensors, and switched outputs. A remote antenna, protected power input, and modular connectors address practical installation problems, while the accompanying software connects the board to mobile and self-hosted services.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/MDB_Slave_ESP32_S3_WROOM_1U_4_layer_cashless_telemetry_board_for_vending_mac_cb2e3ef8.html)

### ESP32-C5 Receives 5 GHz Analog FPV Video

A small ESP32-C5 board now receives 5 GHz analog FPV video through software-defined radio processing. C5VRX demodulates the FM signal and feeds a simple resistor-ladder DAC. Its low-cost hardware makes a useful receiver possible, but latency, sensitivity, range, and video quality still need testing for real FPV flying.

**Source →** [hackaday.com](https://hackaday.com/2026/10/20/5-ghz-drone-video-with-an-esp32/)

## IoT

### A Proximity Interlock for Machine Safety

A MAX32630FTHR based prototype watches for people near moving machinery, then links detection to an alarm and shutdown response. The schematic shows how sensing, control logic, indicators, and the machine interface work together, while the project also makes clear why certified industrial safety hardware needs more safeguards.

**Source →** [electronicsforu.com](https://www.electronicsforu.com/electronics-projects/smart-industrial-machine-safety-control-system-for-human-proximity-detection-and-accident-prevention)

### Build Offline Sound Awareness Aid with Arduino UNO Q

For people who cannot rely on hearing, AudioSense offers a practical starting point: a microphone, MAX9814 amplifier, Arduino UNO Q, and local sound classification. The prototype aims to identify important environmental sounds and provide awareness alerts without sending captured audio to an online service.

**Source →** [electronicsforu.com](https://www.electronicsforu.com/electronics-projects/digikey-contest/audiosense-an-offline-edge-ai-sound-awareness-device-for-the-deaf-and-hard-of-hearing)

## Raspberry Pi

### Small Boards, Big Builds: Raspberry Pi Zero Projects

A tiny Linux board can run far more than a desktop experiment. This project roundup gathers Raspberry Pi Zero builds for portable, wearable, networked, gaming, and discreet applications, with the Pi Zero W adding wireless access. Each linked tutorial provides its own wiring, Python code, and construction details.

**Source →** [circuitdigest.com](https://circuitdigest.com/raspberry-pi-zero-projects-and-tutorials)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-59)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-59)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-59)

## From the bench

### Wire gauge (AWG) chart

One of 15 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools?utm_source=issue_page&utm_medium=bench&utm_campaign=issue-59)

---

Full issue: https://www.tinkernews.com/issues/59-wireless-relay-stations-esp32-audio-docks-and-5-ghz-fpv · Subscribe: https://www.tinkernews.com
