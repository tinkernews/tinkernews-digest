# TinkerNews #56: ESP32 Fall Detectors, Aircraft Radar, and Gesture Gloves

Issue 56 brings hands-on ESP32 builds into the real world: a wearable fall detector that sends WhatsApp alerts, a standalone aircraft radar console, and a gesture-controlled…

*Issue #56 · 2026-10-05*

## Arduino

### Wearable ESP32 Fall Detector Sends WhatsApp Alerts

A wearable XIAO ESP32-S3 pairs with an MPU6050 to spot likely falls, confirm ten seconds of immobility, and send a WhatsApp message through CircuitDigest Cloud. This hands-free build includes wiring, firmware, parts, and a 3D-printed case, while noting limits such as connectivity, calibration, and false alarms.

**Source →** [circuitdigest.com](https://circuitdigest.com/microcontroller-projects/elderly-fall-detection-system-using-esp32)

### Wall-Mounted ESP32 Touchscreen with Wireless Relay Control

A VIEWE ESP32-S3 touchscreen forms the wall-mounted interface, while a second ESP32 runs four relays and reads a DHT22. ESP-NOW links both boards without a dedicated cable. ESPHome brings local temperature and humidity, OpenWeather forecasts, Open-Meteo UV data, and NTP time into one practical control panel.

**Source →** [maker.pro](https://maker.pro/arduino/projects/esp32-touchscreen-home-automation-control-panel-esphome)

### Build an ESP32 Aircraft Radar Console

A small ESP32, 1.8-inch TFT, and Wi-Fi connection form FlyRadar32, a desktop aircraft display fed by OpenSky data. The build covers verified wiring, breadboard testing, browser-based firmware installation, resilient telemetry handling, weather and diagnostics screens, and a FreeCAD-designed printed case for the finished console.

**Source →** [skrelectronicslab.com](https://skrelectronicslab.com/flyradar32-standalone-esp32-ads-b-aircraft-radar/)

### Arduino Five-Antenna Selector Uses CAT and BCD

Manual antenna changes become tedious when an operator moves across HF bands. This Arduino controller accepts either CAT serial data or BCD signals, selects one of five antenna paths, shows the result on a seven-segment display, and sounds a buzzer when the band changes. Check the full design before transmitting.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/Automatic_Five_Antenna_Selector_with_Both_CAT_and_BCD_Decoding_55d8ad9a.html)

### Use a BJT to Drive a 12V MOSFET from Arduino

A 5V Arduino pin is not a power switch. This circuit uses a BJT as an intermediate level-shifting stage, then lets a MOSFET handle current from a separate 12V supply. The arrangement suits lights, fans, relays, and other loads while keeping heavy current away from the microcontroller.

**Source →** [homemade-circuits.com](https://www.homemade-circuits.com/how-to-connect-bjt-and-mosfet-with/)

### Build an Uno with a Built-In MPU-6050

A custom KiCad board combines the familiar Arduino Uno R3 SMD-compatible layout with an onboard MPU-6050 six-axis IMU. The design handles 5 V-to-3.3 V I²C signaling, keeps the sensor underneath the PCB, and removes the separate breakout board, loose wires, and mounting work from compact motion projects.

**Source →** [elecrow.com](https://www.elecrow.com/sharepj/arduino-uno-imu-1506.html)

## 3D Printing

### Set Up Automatic Multi-Color Printing on a QIDI Q2

Four loaded spools, one heated box, and QIDI Studio handle the color changes for a QIDI Q2. This walkthrough covers wiring, drying, spool checks, slicing, waste, material limits, and recovery when an automatic filament change fails during a long print.

**Source →** [qidi3d.com](https://qidi3d.com/blogs/guides/how-to-setup-multi-color-3d-printing)

## DIY Electronics

### FaderBuddy Makes Motorized Faders Modular

Motorized faders often need custom drivers and timing code. FaderBuddy puts that work on an ATtiny1616, turning a 60 mm slider into an I2C peripheral. A host can read positions, set targets, add virtual detents or haptic feedback, and connect several boards to one bus.

**Source →** [github.com](https://github.com/scottbez1/FaderBuddy)

### Build a $10 ESP32 Flock Camera Detector

An ESP32 listens to nearby Wi-Fi traffic without joining the network, then checks documented signatures linked to Flock Safety cameras. The project offers a $9–11 solderless build, optional custom PCB, configurable alerts, and GPS mapping. Results still need local testing, and wireless monitoring laws and privacy rules apply.

**Source →** [github.com](https://github.com/simeononsecurity/flock-you-esp32)

### Project Hydra: An Open 1 W LoRa PCB for Meshtastic

Project Hydra gives makers an editable KiCad design for a minimalist 1 W LoRa board intended for Meshtastic. The public repository includes schematic, layout, and revision history, making it useful for study or adaptation. Check today’s files, hardware details, regulations, and GPL-3.0 requirements before building.

**Source →** [protoflow.ai](https://www.protoflow.ai/community/references/project-hydra-meshtastic-pcb)

## ESP32

### A Gesture-Controlled ESP32 Glove for 3D Building

Away from a desk, a phone can still become a 3D workspace with Aloft: a glove uses MPU-6050 sensors and two ESP32 boards to send hand motion over Bluetooth. Tilting moves through X, Y, or Z, while aiming and tapping place pieces or carve shapes in the browser or iPhone app.

**Source →** [devpost.com](https://devpost.com/software/aloft)

### Build an ESP32-S3 Bambu Lab Printer Monitor

A small color screen beside the printer can show temperatures, progress, and events without opening a phone or browser. BambuHelper pairs an ESP32-S3 with an ST7789 TFT, MQTT, and optional buzzer, offering LAN or cloud connections, browser setup, several board choices, and clear credential trade-offs.

**Source →** [github.com](https://github.com/Keralots/BambuHelper)

### How FlipDeFlock Maps Nearby Surveillance Signals

Pairing a Flipper Zero with an ESP32 lets FlipDeFlock listen for several kinds of surveillance equipment without transmitting. Probe-request fingerprints can point to likely randomized-MAC cameras, while Remote ID, BLE, and other broadcasts add context. Results remain clues, so visual checks and authorized use are essential.

**Source →** [github.com](https://github.com/ReconGrunt/FlipDeFlock)

## IoT

### WiFi Sensing Turns Routers Into Room Monitors

Radio reflections become the input for RuView, an open-source WiFi sensing project that estimates presence, movement, breathing, and heart rate without cameras or wearables. Its visualization and smart-home links make it interesting for makers, but hardware support, accuracy, privacy, and medical limits need careful checking before deployment.

**Source →** [github.com](https://github.com/ruvnet/RuView?ref=repotrend.com)

## Raspberry Pi

### Build a Raspberry Pi MQTT Hub with Mosquitto

A Raspberry Pi can serve as the local message hub for ESP32s, Shelly devices, and home-automation tools. Install Mosquitto, secure its broker, and use MQTT Explorer to check traffic. Home Assistant, Node-RED, and new sensors can share data without custom point-to-point links.

**Source →** [raspberry.tips](https://raspberry.tips/en/smart-home/mqtt-raspberry-pi-mosquitto)

---

Full issue: https://www.tinkernews.com/issues/56-esp32-fall-detectors-aircraft-radar-and-gesture-gloves · Subscribe: https://www.tinkernews.com
