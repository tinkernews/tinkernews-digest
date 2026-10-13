# TinkerNews #57: Duck Robots, OpenScopes, and ESP32 Haldex Controllers

Issue 57 explores a printable fifteen-servo duck robot, reverse-engineered FNIRSI OpenScope firmware, and an ESP32-S3 controller for VAG Haldex systems—plus practical Raspberry…

*Issue #57 · 2026-10-12*

## Raspberry Pi

### Python GPIO Projects for Raspberry Pi LEDs and Buttons

A small Raspberry Pi lab starts with a blinking LED, then adds button input, event responses, and brightness control. The guide compares gpiozero, lgpio, and RPi.GPIO, explains Pi 5 compatibility, and includes wiring advice, installation steps, runnable Python examples, interrupts, and PWM for practical physical computing.

**Source →** [raspberry.tips](https://raspberry.tips/en/raspberrypi-tutorials/raspberry-pi-gpio-python)

### Find and Reclaim Raspberry Pi Storage

A Raspberry Pi can fail quietly when its SD card or SSD fills up. This guide gives you a safe sequence using `df -h`, `sudo ncdu -x /`, and `sudo apt clean`, then covers logs, packages, project files, inodes, and hidden open files so you can clean the right data.

**Source →** [raspberry.tips](https://raspberry.tips/en/raspberrypi-tutorials/free-up-storage-raspberry-pi)

### Run Embedded Boards in Your Browser

Velxio brings embedded coding and circuit testing into a browser window. Pick a board, write Arduino C++, MicroPython, ESP-IDF, or Python, connect virtual parts, and run the program through CPU emulation. It is useful for lessons, early firmware checks, and experiments when physical hardware is unavailable.

**Source →** [github.com](https://github.com/davidmonterocrespo24/velxio)

## DIY Electronics

### Build a Low Cost Solar Car That Moves

Sunlight can move a lightweight homemade car when a small photovoltaic panel feeds a DC motor directly. This quick build uses inexpensive parts, then becomes a useful test platform for light levels, panel angles, wheel sizes, friction, and gearing. Record speed, compare results, and present the evidence with simple graphs.

**Source →** [spheralsolar.com](https://spheralsolar.com/build-a-solar-powered-car-that-actually-wins-your-science-fair/)

### OpenScope Replaces Buggy FNIRSI 2C53T Firmware

Live waveforms now appear from a FNIRSI 2C53T running software built from scratch through reverse engineering. OpenScope brings up the AT32 microcontroller, configures the Gowin FPGA, captures real probe signals, and renders them without the factory firmware. Flashing still carries serious risks, including lost calibration and unusable hardware.

**Source →** [github.com](https://github.com/DavidClawson/OpenScope-2C53T)

### Build a ROS 2 Rover with ESP32 or Pico

Linorobot2 puts the electronics and firmware for a ROS 2 mobile robot on familiar ESP32s and Raspberry Pi Picos. It links motor control and odometry to ROS 2, with USB or Wi-Fi communication, OTA updates, and network diagnostics. The repository still expects its wiki for wiring and bring-up details.

**Source →** [github.com](https://github.com/linorobot/linorobot2_hardware)

### Build an ESP32-S3 Haldex Controller for VAG Cars

Factory Haldex systems can be difficult to inspect or tune. OpenHaldex-S3 uses an ESP32-S3, an inline harness, and public firmware to add browser-based setup, diagnostics, logging, and tuning for supported VAG vehicles. This MIT-licensed project is separate from the newer proprietary OpenHaldex SS application and its installer.

**Source →** [github.com](https://github.com/meatro/OpenHaldex-S3)

### Build a Printable Duck Robot for Motion Experiments

Print a duck-shaped biped, fit its fifteen serial servos, and connect the controller board to make XGO-Duck move. The open hardware project guides builders from parts and electronics preparation through assembly, browser-based calibration, and reinforcement-learning experiments with balance, walking, and custom robot behaviors.

**Source →** [github.com](https://github.com/LuwuDynamics/xgoduck_hardware)

### Arduino Metal Detector with Target Classification and Depth

A hand wound coil, paired oscillators, and an Arduino turn small frequency shifts into a useful metal detection display. The project separates likely ferrous and non ferrous targets, estimates depth zones, and keeps the sensing process visible through calibration data, an LCD, and practical tests.

**Source →** [projectech.in](https://projectech.in/projects/metal-detector-project-target-discrimination-arduino/)

## ESP32

### Build Room by Room Home Assistant Touch Panels

Tessera turns affordable ESP32 color touchscreens into dedicated Home Assistant panels for each room. Choose a supported display, install its Screen Manager add-on, design a shared dashboard, and deploy it across your home. Lights, climate, media, locks, blinds, weather, and vacuum controls can all fit in one interface.

**Source →** [github.com](https://github.com/MaxGramser/homeassistant_espscreen)

### Rewire a SmallTV for Stocks, Claude, and Planes

Replace a GeekMagic SmallTV’s stock software and its tiny color screen becomes a Wi-Fi dashboard for prices, Claude usage, and nearby aircraft. One codebase supports several ESP variants, while a web interface handles settings, mode selection, and wireless updates. The result is a compact, practical firmware project.

**Source →** [github.com](https://github.com/giovi321/smalltv-mod)

### Turn Waveshare Industrial I/O Into a Network Controller

Eight isolated inputs, eight outputs, Ethernet, and PoE give Waveshare’s ESP32-S3 I/O boards a solid hardware base. Open firmware adds MQTT, Modbus RTU, CAN bus, local JavaScript rules, web settings, and an optional Matter build, while separate applications keep memory limits manageable.

**Source →** [github.com](https://github.com/hennejg/waveshare-ESP32-S3-io)

## IoT

### ESP32-C6 RMT Drives a Reliable WS2812 LED

On an ESP32-C6-DevKitC-1, the onboard WS2812 LED receives a carefully timed 24-bit color frame from the RMT peripheral. This hardware approach keeps sub-microsecond pulses steady while FreeRTOS and wireless handlers run, then checks the frame timing through the serial console for a practical embedded IoT test.

**Source →** [hubble.com](https://hubble.com/community/guides/how-to-drive-addressable-leds-with-the-esp32-c6-rmt-peripheral/)

### ESP32 Arduino IDE Troubleshooting Checklist

When an ESP32 refuses to appear, compile, or accept a sketch, this practical guide helps separate IDE setup, upload, power, and silicon revision problems. It covers current Arduino IDE installation across Windows, macOS, and Linux, plus board selection and errata. It is not a complete device build.

**Source →** [randomnerdtutorials.com](https://randomnerdtutorials.com/esp32-troubleshooting-guide/)

## Robotics

### Build an Open Source Robot Vacuum for $200

A work in progress called OOMWOO breaks a robot vacuum into affordable, replaceable parts: drive modules, a caster, suction hardware, sensors, and Raspberry Pi control. Its roughly $200 parts goal is promising, but matching commercial navigation and cleaning still depends on mechanical fit, electronics, software, and testing.

**Source →** [github.com](https://github.com/makerspet/oomwoo/blob/main/BOM.md)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-57)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-57)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-57)

## From the bench

### WS2812B power calculator

One of 15 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools?utm_source=issue_page&utm_medium=bench&utm_campaign=issue-57)

---

Full issue: https://www.tinkernews.com/issues/57-duck-robots-openscopes-and-esp32-haldex-controllers · Subscribe: https://www.tinkernews.com
