# TinkerNews #53: Smarter, Safer, More Local Builds

Build an offline Arduino AI agent, a calibrated digital level, Raspberry Pi power and recording projects, ESP32 home-control tools, a Klipper toolchanger, a printed microreactor…

*Issue #53 · 2026-09-15*

## Arduino

### An Offline Arduino Agent That Understands Plain English

Type a plain-English instruction into an Arduino App Lab project, and a local language model on the UNO Q can direct connected hardware. This hands-on build combines Modulino sensors and outputs, showing how behavior can change through new sentences rather than firmware changes, without internet access or API keys.

**Source →** [projecthub.arduino.cc](https://projecthub.arduino.cc/hardik_chadda/talk-to-your-arduino-build-an-on-device-ai-agent-in-arduino-app-lab-0265ba)

### Arduino Two-Axis Level With Zero Reference

A bubble level can check one surface, but this handheld Arduino tool can compare two. An ADXL345 feeds gravity readings to a Nano, which shows pitch and roll on an OLED. Press ZERO on one bracket, then match that stored angle on another—even when both are intentionally sloped.

**Source →** [learniot.in](https://learniot.in/arduino-adxl345-digital-level/)

## 3D Printing

### MedusaHC: Open-Source Python Toolchanger for Klipper

MedusaHC adds automatic hotend changes to a Klipper printer through an open-source mechanical system and Python controller. The beta project coordinates pickup, parking, feeding, priming, cleaning, and sensor checks, while keeping familiar commands. It suits careful makers testing multi-material setups, but requires mechanical work, calibration, and the repository’s installation guide.

**Source →** [github.com](https://github.com/Irbis3D/MedusaHC)

### Build a Low-Cost 3D-Printed AirFlow Microreactor

At about £100, the AirFlow microreactor uses a printed chamber, forced hot air, and Arduino control to hold LAMP reactions near a steady temperature. The Biomaker project hub presents it as an evolving open build, with downloadable files and practical notes for classrooms, community labs, and DIY researchers.

**Source →** [biomaker.org](https://biomaker.org/project-logs)

## ESP32

### Hestia32: An Open Thermostat for Multi-Stage HVAC

Hestia32 puts local control at the center of a repairable thermostat for varied HVAC systems. Its ESP32-C5, SHT45 sensor, touchscreen, configurable relays, MQTT support, and OTA updates work without a cloud subscription. Thread, Matter, Zigbee, and complete build files are planned, but the project remains in development.

**Source →** [hackaday.io](https://hackaday.io/project/206638-hestia32-open-source-smart-thermostat)

### Turn a Sonoff NSPanel into Local Control

The Sonoff NSPanel EU can do more than control eWeLink devices. With ESPHome on its ESP32 and Home Assistant as the local controller, its touchscreen, buttons, relays, and temperature sensor become useful across a wider home system. Flashing takes care, and the 240 V terminals require serious electrical safety.

**Source →** [jirkovynavody.cz](https://jirkovynavody.cz/en/homeassistant/integrations/sonoff-nspanel/)

## IoT

### Sync Home Assistant Lights With the Sun

Static brightness and color settings can make a smart home feel out of step with the day. Adaptive Lighting uses Home Assistant’s sun data to set cooler, brighter daytime light and warmer, dimmer evening light, while keeping manual controls available and requiring no custom lighting hardware.

**Source →** [github.com](https://github.com/basnijholt/adaptive-lighting)

### Turning Huawei Solar into Home Assistant Data

Solar equipment can report far more than a single production number. This Home Assistant integration reads supported Huawei Solar data and functions through Modbus, then presents them as entities for dashboards and automations. Setup depends on compatible hardware, a reachable interface, correct addressing, and sensible polling intervals.

**Source →** [github.com](https://github.com/wlcrs/huawei_solar)

### Build Long-Running ESP32 Sensor Nodes with Deep Sleep

Battery life depends on more than an ESP32’s sleep-current figure. This practical guide lays out a wake, measure, transmit, and sleep pattern for soil monitors, weather stations, and other remote devices, while covering wake sources, retained state, wireless costs, board leakage, and realistic runtime estimates.

**Source →** [iotjournal.net](https://iotjournal.net/esp32-deep-sleep-battery-guide/)

## Raspberry Pi

### Raspberry Pi 5 UPS with Modular Battery Protection

This open hardware build pairs removable NP-F batteries with USB-PD power electronics to keep Raspberry Pi projects running through brief outages or shut them down safely. An OLED, firmware, and printed enclosure make it a complete maker project, while its documented limits still need checking.

**Source →** [github.com](https://github.com/Web3-Pi/Web3-Pi-UPS)

### PEBBLE: A Raspberry Pi Recorder in a Rock

A small pebble-shaped case hides a complete voice recorder built around a Raspberry Pi. PEBBLE brings microphone wiring, audio capture, file storage, portable battery power, controls, and enclosure design into one compact project, giving makers a clear example of turning general-purpose Linux hardware into a focused handheld tool.

**Source →** [instructables.com](https://www.instructables.com/PEBBLE-Portable-Audio-Recorder/)

### Build an OpenFlight Controller with Raspberry Pi

OpenFlight brings Raspberry Pi computing, GPIO wiring, UART serial communication, diagnostics, and a custom enclosure into one flight-electronics project. The repository shows an active build, but exact boards, peripherals, wiring, and software steps still need checking before assembly. Much of the work lies in making every part fit and communicate reliably.

**Source →** [github.com](https://github.com/open-flight/openflight)

### Build an Open-Hardware IP-KVM for Remote Computer Control

A stuck computer does not have to mean a trip to the machine. ESPKVM combines network video access with remote keyboard and mouse control, using custom board designs around HDMI capture and USB. Its schematics, board targets, and automation history give makers a useful starting point, pending hardware verification.

**Source →** [github.com](https://github.com/espkvm/espkvm)

## Robotics

### Build an Open-Source ADS-B Receiver for Nearby Aircraft

A compact board can turn aircraft broadcasts into useful local data without the usual Raspberry Pi and SDR pair. ADSBee combines 1090 MHz reception and decoding in an open-source, low-power design, giving makers a practical base for portable trackers, custom displays, field experiments, and community aircraft-data stations.

**Source →** [makezine.com](https://makezine.com/article/drones-vehicles/planes/track-aircraft-with-adsbee-an-open-source-ads-b-receiver/)

---

Full issue: https://www.tinkernews.com/issues/53-smarter-safer-more-local-builds · Subscribe: https://www.tinkernews.com
