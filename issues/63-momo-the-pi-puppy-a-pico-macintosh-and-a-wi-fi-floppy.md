# TinkerNews #63: Momo the Pi Puppy, a Pico Macintosh, and a Wi Fi Floppy Archive

This issue has a Raspberry Pi puppy companion, a tiny Pico Macintosh, a Wi Fi reader for camera floppy disks, a blind corner warning system, OLED displays, smart home sensors…

*Issue #63 · 2026-11-24*

## Arduino

### CornerSense Maps Motion Around a Blind Corner

CornerSense uses paired infrared checkpoints to estimate whether an object is approaching a blind corner, how fast it moves, and when it may arrive. An Arduino handles sensing and local alerts, while a Raspberry Pi provides a dashboard and ThingSpeak logging for this educational tabletop prototype.

**Source →** [instructables.com](https://www.instructables.com/CornerSense-a-Blind-Corner-Warning-System-With-Ard)

### Arduino SH1106 OLED Interface Over I2C

Four wires connect an Arduino Uno or Nano to a readable 1.3-inch SH1106 OLED. This practical build covers the correct library, power, I2C address scanning, buffered drawing, live counters, shapes, icons, and bitmaps. It also explains memory limits and common fixes when the screen stays blank.

**Source →** [controllerstech.com](https://controllerstech.com/arduino-sh1106-oled-display-tutorial/)

### Arduino SSD1306 OLED: Wiring to Animation

Four wires give an Arduino a 128x64 screen for greetings, counters, sensor readings, icons, logos, and simple animations. This build covers I2C wiring, address scanning, Adafruit library setup, buffered drawing, bitmap storage, and memory limits, with examples that grow from a first message into a small device interface.

**Source →** [controllerstech.com](https://controllerstech.com/arduino-ssd1306-oled-display-tutorial/)

### Run Laya Decisions on the Arduino UNO Q

A Python app runs Laya locally on the Arduino UNO Q and routes requests to fixed choices, checks whether something is broken, or scores urgency. The build uses CPU-only PyTorch, manages a 322 MB model within 4 GB of RAM, and can reject uncertain answers before they trigger an action.

**Source →** [mischianti.org](https://mischianti.org/arduino-uno-q-laya-decision-model/)

## 3D Printing

### Snapmaker U1 Toolhead Swaps in 30 Seconds

A Snapmaker U1 firmware fork keeps nozzle, flow, PID, and offset data with each physical toolhead instead of its slot. USB serial detection, selective calibration, and a guided swap process simplify changes. The mod also needs supported USB-C cables, printed strain relief, careful installation, and cautious testing.

**Source →** [github.com](https://github.com/rando-calrissian/SnapmakerU1-Extended-Firmware-Mod-Virtual-Toolheads)

## DIY Electronics

### Portable Fuzzy Logic on Embedded Boards

A fuzzy model can stay in a file while one MATLAB-generated inference engine moves between boards. This project connects that approach to STM32, SAM3X8E, Raspberry Pi, and ESP32 applications, showing the value of reusable code alongside the memory, parser, storage, and validation work embedded deployments require.

**Source →** [mdpi.com](https://www.mdpi.com/2079-9292/15/22/5297/pdf)

### A 16-LED Heart on a Rechargeable Nano

Sixteen LEDs form a heart on a 50 × 70 mm perfboard, with an Arduino Nano controlling nine patterns. A LiPo, protected TP4056 charger, MT3608 voltage converter, battery sensing, and removable headers turn the keychain into a compact embedded project with careful power and wiring requirements.

**Source →** [github.com](https://github.com/engineerdiaa/portable-heart-led)

### A Wi-Fi Archive for Camera Floppy Disks

Old camera disks get a second life in floppy3.5, a battery-powered reader that turns 3.5-inch FAT12 media into Wi-Fi photo archives. An RP2354A handles the drive, an ESP32-S3 serves floppy.local, and a microSD card stores files without confusion when cameras reuse filenames.

**Source →** [github.com](https://github.com/bigcrimping/floppy3.5)

## ESP32

### An Offline ESP32-S3 Learning Lab

Datasheets, pinout diagrams, firmware files, and tutorials often live in separate places. esp-labs-web brings them together as a browser-based ESP32-S3 study lab, with lessons, interactive widgets, code tours, references, and offline access. Its companion esp-labs checkout supplies the firmware content behind the learning experience.

**Source →** [github.com](https://github.com/agharsallah/esp-labs-web)

### Tesserae Turns E-Ink Panels Into Thin Clients

One Tesserae server can feed a house full of e-ink panels, from always-on Raspberry Pi displays to battery ESP32 boards. Browser-authored HTML becomes a calibrated, panel-ready frame on the server, while each client fetches or receives packed bytes, reports its status, refreshes the screen, and sleeps.

**Source →** [github.com](https://github.com/dmellok/tesserae)

### ESP32 Digital Tube-Sound Processor

An ESP32, WM8960 codec, color display, and three rotary encoders form a compact processor for digitally shaped audio. It separates ordinary tone controls from nonlinear harmonic processing, with presets, a startup graph, and spectral analysis of the second harmonic. The project reuses hardware and software from an earlier parametric equalizer.

**Source →** [hackaday.io](https://hackaday.io/project/207347-esp32-tube-sound-processor-warm-analog-sound)

### Build a $10 ESP32-C3 NFC Access Controller

Around $10 in parts gets you Prismo, a self-hosted NFC controller for doors, machines, and other relay loads. An ESP32-C3 reads card UIDs through a PN532, checks authorization over MQTT, gives local LED and buzzer feedback, and switches a relay from a single-layer, maker-friendly PCB.

**Source →** [github.com](https://github.com/nu31hackerspace/prismo/)

## IoT

### Turn an Android Tablet Into a Home Assistant Hub

An old Android tablet can become a Home Assistant control panel, voice satellite, music screen, camera sensor, and room display with Kiosk Satellite. The app keeps dashboards, voice features, timers, media controls, screensavers, and selected device sensors together, while optional Ground Control handles heavier voice processing nearby.

**Source →** [github.com](https://github.com/jxlarrea/kiosk-satellite)

### Migrating ESP32 Devices to Hybrid Post Quantum TLS

An ESP32 starts with classical TLS, then receives a signed firmware image that enables hybrid ML-KEM TLS over the air. A custom Mosquitto bridge connects the device to AWS IoT Core, while cloud services handle certificates, builds, migration steps, telemetry, and dashboard status for the workshop.

**Source →** [github.com](https://github.com/aws-samples/sample-aws-iot-pqc)

### Bring Vehicle Telemetry into Home Assistant

Your car can appear in Home Assistant with live engine data, trip records, parking location, and diagnostic events. Car 2 Home sends readings from an ELM327 adapter through its phone app and a persistent WebSocket. The custom integration creates vehicle sensors, events, and automations without MQTT or a cloud relay.

**Source →** [github.com](https://github.com/car2home/car2home-homeassistant)

### Local EV Charging Control for Home Assistant

A Tuya EV charger can become a local part of Home Assistant with this integration. It uses tinytuya over LAN, then combines grid meters, solar surplus, battery state, tariffs, vehicle history, and safety limits. The interesting work is the control logic around real household conditions.

**Source →** [github.com](https://github.com/lachand/EV_charger)

## Raspberry Pi

### Momo Turns a Pi Into a Puppy

A Raspberry Pi 5 becomes Momo, a German Shepherd-shaped desk companion with puppy sounds, voice AI, physical buttons, and a retro-gaming mode. The build combines a custom printed shell, HDMI display, microphone, I2S audio, cloud services, and downloadable fabrication files in one compact device.

**Source →** [instructables.com](https://www.instructables.com/Momo-Cute-Desk-Companion-That-Barks-in-AI-Plays-Re/)

### SIMUT: Pico W Telemetry With Custom Sensor Hardware

Sixteen sensor slots, a custom PCB, and local display support define SIMUT, an open-source monitoring platform for Raspberry Pi Pico W and Pico 2 W boards. Its repository combines firmware, KiCad files, command-line controls, language packs, fabrication outputs, and tests, while leaving hands-on wiring details for further inspection.

**Source →** [github.com](https://github.com/angeloINTJ/simut)

### Turn a Pico 2 W into a Home Assistant Sensor

A Pico 2 W can report chip temperature, Wi-Fi strength, uptime, and LED state to Home Assistant from a short ESPHome YAML file. You flash it once over USB, then make later changes wirelessly. The setup needs a W model, a data cable, Home Assistant, and 2.4 GHz Wi-Fi.

**Source →** [raspberry.tips](https://raspberry.tips/en/smart-home/raspberry-pi-pico-with-esphome-home-assistant)

### OpenScreens Turns Apple Devices into Raspberry Pi Remotes

OpenScreens puts a Raspberry Pi desktop on an iPhone, iPad, or Mac through VNC. Enable the Pi's VNC server, add its address and credentials, then connect locally or through SSH or Tailscale. Touch gestures, trackpad mode, compatibility tests, and saved sessions make remote Pi access practical.

**Source →** [github.com](https://github.com/burakgon/OpenScreens)

### A 62 mm Raspberry Pi Pico Macintosh

At 62 mm tall, pico-mac-nano runs a Macintosh 128K emulator on an RP2040 Pico Zero. A custom PCB, portrait TFT, micro-SD storage, USB input, audio, and optional battery fit inside a printed case. The project includes firmware, source, board files, disk images, and printable parts for makers who enjoy tight constraints.

**Source →** [github.com](https://github.com/all2coolnick/pico-mac-nano)

## Robotics

### Build a Sim Racing Seatbelt Tensioner

Braking in a racing simulator can pull both shoulder belts against the driver with this open-source dual-channel build. ESP32-S3 boards, iSV57 servos, linear modules, and SimHub data work together, while sensorless homing, automatic parking, and current monitoring handle motion control without external limit switches.

**Source →** [github.com](https://github.com/ChrGri/DIY-Sim-Racing-FFB-BeltTensioner)

### MARS Builds One Rover Base for Many Jobs

Two decks, four motors, and separate payload controllers make MARS a practical rover prototype. An Arduino Uno handles Bluetooth driving and obstacle stopping, while Raspberry Pi and Nano modules add video and environmental sensing. The design works, though shared power, data links, firmware, and autonomous navigation remain unfinished.

**Source →** [circuitdigest.com](https://circuitdigest.com/microcontroller-projects/diy-arduino-bluetooth-robot)

### Lyapunov Unifies Robot Scenes, Physics, and Camera Data

A desktop workspace can take a robot model from scene setup to bounded control and calibrated camera capture. Lyapunov combines files, code, terminals, physics, annotations, and dataset tools under Apache-2.0. It remains software-heavy, so advanced engines, renderers, assets, policies, and hardware may need separate setup.

**Source →** [github.com](https://github.com/ManfredCh/Lyapunov)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-63)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-63)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-63)

## From the bench

### ESP32-C3 SuperMini pinout

One of 19 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools)

---

Full issue: https://www.tinkernews.com/issues/63-momo-the-pi-puppy-a-pico-macintosh-and-a-wi-fi-floppy · Subscribe: https://www.tinkernews.com
