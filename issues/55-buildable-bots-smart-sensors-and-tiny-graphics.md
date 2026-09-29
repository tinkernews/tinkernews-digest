# TinkerNews #55: Buildable Bots, Smart Sensors, and Tiny Graphics

Issue 55 explores hands-on maker projects: an ESP32-S3 rendering N64-style worlds, Raspberry Pi robots and CAN-bus tools, ESP32 environmental monitors and RC cars, plus open…

*Issue #55 · 2026-09-28*

## Raspberry Pi

### Build a Raspberry Pi Thermal Printer

A Raspberry Pi, a small thermal printer, and a few Python files can turn digital messages into paper. This repository provides a practical starting point, with wiring documentation and active development, but its current README and source should be checked for exact hardware, power, and connection details.

**Source →** [github.com](https://github.com/MoritzHayden/momir-basic-printer)

### Garden of Eden Puts a Raspberry Pi in Control

Closed garden systems can leave useful hardware tied to one controller. Garden of Eden takes a different route: a Raspberry Pi runs local software, reads environmental sensors, connects garden hardware through GPIO, and feeds Home Assistant. It remains a work in progress, but offers a practical path toward inspectable, adaptable control.

**Source →** [github.com](https://github.com/iot-root/garden-of-eden)

### Raspberry Pi Touchscreen Aircraft and Marine Tracker

A Raspberry Pi and 4-inch touchscreen present nearby aircraft and marine traffic as a compact radar-style display. The project pairs relative positions with map views, but the supplied repository excerpt does not confirm the Pi model, touchscreen connection, enclosure, receivers, APIs, or startup procedure, so those details need checking before building.

**Source →** [github.com](https://github.com/yashmulgaonkar/FlightScnr_Pi)

### Poké Pi: A Raspberry Pi Poké Ball Cyberdeck

A red-and-white Poké Ball shell houses this custom Raspberry Pi gaming console. Designed for classic Pokémon and other retro games, the project pairs Fusion 360 enclosure work with Gen 1 Recomp software. Its photos show a themed handheld taking shape, while several hardware details still require confirmation.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/Pok_Pi_Cyberdeck_d4507a91.html)

### Give an AI a Body: Raspberry Pi Robot

A Raspberry Pi can serve as an AI brain while a PiDog supplies the legs, camera, microphone, speaker, and motors. This open-source project links both sides over HTTP, supports hosted or local language models, and adds face recognition, speech, movement, and Telegram control across a network.

**Source →** [github.com](https://github.com/rockywuest/pidog-embodiment)

### Build a Raspberry Pi CAN-Bus Reverse-Engineering Lab

Raw CAN frames rarely explain themselves. CanLab pairs a Raspberry Pi logger with a Python/PyQt6 desktop workstation that helps inspect traffic, test candidate signals, and export DBC files. Its suggestions are heuristic, so validation matters, and replay or injection belongs only on an isolated bench—not in a road vehicle.

**Source →** [github.com](https://github.com/Sherin-SEF-AI/CanLab)

### Build the Open Duck Mini v2

Fifty-one printed parts turn the Open Duck Mini v2 into a practical Raspberry Pi robotics project. Its 36 STL files, wiring diagrams, and guides cover much of the path from printed feet to walking software. You still need to check fits and print settings, since the source reports no physical validation.

**Source →** [microduckrobot.org](https://microduckrobot.org/diy/open-duck-mini/)

## Arduino

### How an ESP32-S3 Renders N64-Style Megatextures

A custom software renderer lets an ESP32-S3 move through a textured 3D scene without a dedicated GPU. The project fits its megatexture data into 16 MB of PSRAM by using 8-bit indexed color, showing how mipmaps, compression, and careful memory choices support console-style graphics on small hardware.

**Source →** [hackaday.com](https://hackaday.com/2026/09/28/jet-megatextures-demo-for-esp32-s3/)

## DIY Electronics

### Add Motorized Faders Over Two I2C Pins

Several motorized sliders usually mean extra drivers, feedback wiring, and GPIO use. FaderBuddy puts that work on a modular board for 60 mm faders, with an ATtiny1616 handling motion locally. One I2C bus can serve multiple boards, while ESPHome connects the controls to Home Assistant with a little YAML.

**Source →** [github.com](https://github.com/scottbez1/FaderBuddy/blob/master/README.md)

## ESP32

### A 3D-Printed Planter That Monitors Indoor CO₂

Behind its geometric planter shell, murCO uses an ESP32-based controller and SCD40 sensor to send local CO₂, temperature, and humidity readings to Home Assistant. LEDs, optional speech, and Bluetooth proxy features make ventilation information useful without depending on a dashboard. The open-source repository and project documentation provide implementation details.

**Source →** [openelab.io](https://openelab.io/blogs/learn/murco-home-assistant-co2-monitor-planter)

### Build an ESP32 Sparkle Motion Light

Tiny points of colored light can feel surprisingly alive when they move, fade, and sparkle independently. This project pairs an ESP32-based Adafruit board with addressable LEDs and CircuitPython, giving makers a hands-on way to build an animated display, then adjust its colors, timing, brightness, and physical form.

**Source →** [cdn-learn.adafruit.com](https://cdn-learn.adafruit.com/downloads/pdf/adafruit-sparkle-motion.pdf)

### Reliable ESP-NOW RC Car With ESP32 and ESP8266

At 2.02 volts, a battery pack exposed the gap between firmware’s “protected” message and real electrical safety. This ESP-NOW RC car pairs an ESP32 controller with an ESP8266 vehicle board, then adds packet checks, acknowledgements, failsafes, pairing, and hard-won debugging lessons from actual hardware faults.

**Source →** [learniot.in](https://learniot.in/esp-now-rc-car-esp32-esp8266/)

## IoT

### ESP32-C3 Super Mini: Wi-Fi Tests and Deep Sleep

Small enough for tight enclosures, the ESP32-C3 Super Mini still offers Wi-Fi, Bluetooth, useful GPIO, and a deep-sleep mode. This hands-on guide moves from pinout and Arduino IDE setup to a local web server and timed wake-up test, showing where the board fits in battery-powered IoT projects.

**Source →** [randomnerdtutorials.com](https://randomnerdtutorials.com/getting-started-esp32-c3-super-mini/)

## Robotics

### reBot-DevArm Opens a Robotic Arm to Makers

Physical manipulation and robot-learning work needs more than a simulator. reBot-DevArm offers an open arm project with hardware under CERN-OHL-W-2.0 and software under Apache-2.0, plus planned links to ROS, LeRobot, and Isaac Sim. Its repository is the starting point, though several build specifications still need checking.

**Source →** [github.com](https://github.com/Seeed-Projects/reBot-DevArm/)

---

Full issue: https://www.tinkernews.com/issues/55-buildable-bots-smart-sensors-and-tiny-graphics · Subscribe: https://www.tinkernews.com
