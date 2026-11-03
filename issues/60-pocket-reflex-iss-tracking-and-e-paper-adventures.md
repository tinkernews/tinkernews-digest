# TinkerNews #60: Pocket Reflex, ISS Tracking, and E-Paper Adventures

Issue 60 brings hands-on builds that turn embedded hardware into playful, practical machines: an ESP32 pocket reflex console, a Raspberry Pi dish that tracks the ISS, and…

*Issue #60 · 2026-11-02*

## Arduino

### Pocket Reflex Console With Three Games

A pocket-sized ESP32-C3 console turns a round display, eight RGB LEDs, and two buttons into three quick games. Lightning Tap measures reaction time, Chase the Light tests tracking and decisions, and Duel Mode pits two players against each other. The build includes breadboard testing, custom wiring, firmware, and a PLA enclosure.

**Source →** [instructables.com](https://www.instructables.com/Short-Attention-Span-I-Built-a-Pocket-Reflex-Train/)

### Build an ESP32 Alarm Clock That Needs a Basket

A mini hoop, ESP32, and IR beam turn snoozing into a shot. This project connects a buzzer, BLE setup, rechargeable battery, custom PCB, and 3D printed mount, while showing how sensor alignment, timing, debounce, antenna clearance, and enclosure design shape a practical interactive device.

**Source →** [instructables.com](https://www.instructables.com/Smart-Basketball-Hoop-Alarm-Clock-ESP32-BLE-Custom/)

### Build an 8-Channel Arduino RC Link

Two Arduino Nano boards pass eight control channels through nRF24L01 radios. Joysticks, potentiometers, and switches become PWM outputs for servos or an ESC. The build includes a hand-made enclosure, downloadable sketches, and clear pin assignments, while leaving range, calibration, failsafe behavior, and interference testing for the builder.

**Source →** [instructables.com](https://www.instructables.com/How-to-Make-a-DIY-8-Channel-RC-Transmitter-and-Rec/)

### Drive a Scratch-Built RC Car Over the Internet

A hand-cut PVC car uses an ESP-01, Firebase, and a phone app to control its motor and steering through an internet connection. Pen refills form the front pivots, a salvaged gearbox adds wheel torque, and a 3S LiPo powers the electronics. Wi-Fi and Firebase settings need configuring first.

**Source →** [instructables.com](https://www.instructables.com/Infinite-Range-RC-Car-Drive-It-From-Anywhere-in-th/)

### A Browser-Controlled 12-DOF Spider Robot

Four printed legs, twelve servos, and two controllers make this spider robot walk, turn, wave, and dance. An ESP32-C3 handles Wi-Fi commands from a browser, while an Arduino Nano manages the servos, foot positions, and gait timing. An OLED adds animated eyes and changing expressions.

**Source →** [robotlk.com](https://robotlk.com/web-controlled-spider-robot-arduino-nano-and-esp32-c3/)

### BLE Retail Display Timer and Tamper Alarm

A shopper lifting a display product starts a 90-second countdown while movement or an unauthorized removal sounds the alarm. Built around an nRF52840, Zephyr RTOS, BLE, and battery backup, the system sends status and tamper alerts to staff phones without store Wi-Fi or cloud services.

**Source →** [instructables.com](https://www.instructables.com/Interactive-Retail-Display-With-Timer-Anti-Theft-A)

## DIY Electronics

### MatTris Arcade Packs Six Games Into 280 LEDs

A second generation MatTris turns a 14×20 RGB matrix, an RP2040 Tiny, and six buttons into a pocket arcade. Tetris, Snake, Pong, Breakout, Car Dodge, and Space Invaders share a custom PCB, rechargeable power, and a tinted acrylic case built around the tiny display.

**Source →** [electronicwings.com](https://www.electronicwings.com/users/ArnovSharma/projects/6965/mattris-arcade)

## ESP32

### Draw Icons and Scroll Text with a MAX7219 Matrix

Eight binary rows make a smiley or heart on one 8×8 matrix, while four chained modules become a scrolling sign. An Arduino UNO sends SPI data through three control lines, with MD_MAX72XX handling graphics and MD_Parola handling text. Keep brightness low on USB, and use level shifting with an ESP32.

**Source →** [informaticait.it](https://www.informaticait.it/en/guide/max7219-8x8-led-matrix-arduino)

### An ESP32 Replaces the Leaf’s Cloud TCU

When NissanConnect EV services disappear, Leaf owners lose remote climate and charging controls. simppeliTCU uses a LilyGO T-2CAN board, protected automotive power, and ESP32-CAN firmware to restore local access through Wi-Fi, MQTT, and Home Assistant. It remains a draft for experienced builders who can handle vehicle wiring and safety.

**Source →** [github.com](https://github.com/fkorhone/simppeliTCU)

## IoT

### Arduino 4WD Robot With Wi-Fi Radar Mapping

Four TT motors carry an Arduino UNO R4 WiFi through an area while a servo turns an HC-SR04 sensor and sends readings to a browser. Floor markers add waypoint cues, and separate batteries keep motor power apart from the controller. The mapping is SLAM-style, with algorithm details left limited.

**Source →** [hackaday.io](https://hackaday.io/project/207196-4wd-slam-radar-2d-robot-car)

### Build an ESP32 TinyML Vibration Monitor

Unexpected machine faults often begin as small changes in vibration. This ESP32 project uses an MPU6050, a compact autoencoder, and local TinyML inference to spot those changes without cloud processing or fault labels. A calibrated threshold, onboard indicator, MQTT messages, and browser dashboard make results easier to watch and test.

**Source →** [projectech.in](https://projectech.in/projects/tinyml-machine-anomaly-detection-using-esp32/)

### Build an ESP32 Home Assistant Touchscreen Panel

A dedicated ESP32 touchscreen gives each room a simple Home Assistant control point. Flash the panel through a browser, connect it to 2.4 GHz WiFi, and arrange local controls from a web page. Lights, scenes, sensors, cameras, media, and climate information can share one screen.

**Source →** [github.com](https://github.com/jtenniswood/espcontrol)

### Gestire: An ESP32 Locker for Shared Lab Equipment

Reserve an FPGA board in Flutter, receive a six-digit PIN, and enter it at an ESP32 locker. Gestire links room and equipment bookings to Flask, SQLite, keypad input, LCD guidance, and relay-controlled compartments, while showing where sensors and stronger recovery would matter in a real installation.

**Source →** [github.com](https://github.com/miguelovila/gestire-smart-locker)

## Raspberry Pi

### Give a Raspberry Pi Pico Precise Stepper Motion

A Raspberry Pi Pico, ULN2003 board, and 28BYJ-48 motor make repeatable positioning approachable with MicroPython. The supplied library handles coil sequences and offers commands for steps, target positions, directions, and angles. External motor power and a home sensor remain important considerations for small robotics, turntables, gauges, and sliders.

**Source →** [randomnerdtutorials.com](https://randomnerdtutorials.com/raspberry-pi-pico-stepper-motor-micropython/)

### A Raspberry Pi Dish Tracks the ISS

A dish on a portable board follows the International Space Station across the sky. A Raspberry Pi Zero W checks pass predictions, cloud cover, and orbital data, then directs two stepper motors through changing azimuth and altitude. The build turns satellite calculations into visible movement and real nighttime observations.

**Source →** [workshop88.com](https://workshop88.com/oldblog/)

### InkQuest Puts Text Adventures on E-Paper

A rotary encoder, e-paper screen, and ESP32-C3 turn each button press into a new story branch. InkQuest keeps five turns of context, asks Gemini for four choices, and shows the result on a low-power display. Its compact PCB, printed case, and sleep mode support roughly 20 hours of estimated use.

**Source →** [instructables.com](https://www.instructables.com/InkQuest-Interactive-Text-Adventure-Game-Using-E-P/)

### Gemma 4 on a 4 GB Raspberry Pi 5

A 4 GB Raspberry Pi 5 runs Gemma 4 E2B offline through LiteRT, with no AI HAT or cloud connection. The model uses about 1.6 GB of RAM and produces roughly 8 output tokens per second. This guide covers setup, storage, cooling, downloads, benchmarks, and the choice between LiteRT and Ollama.

**Source →** [raspberry.tips](https://raspberry.tips/en/kuenstliche-intelligenz/gemma-raspberry-pi-5-litert)

## Robotics

### ESP32 Board for a Robot Fox

Ten servo connections give this ESP32 board a place in a 3D-printed quadruped fox, alongside two DC motor connections, a TFT display, and sensor inputs. The project includes a schematic, Gerber files, and an MPU6050 test sketch for makers developing their own robot electronics.

**Source →** [pcbway.com](https://www.pcbway.com/project/shareproject/Quadruped_Robot_PCB_controller_Esp32_7dd82d1b.html)

## Recommended reads

### ESP32 Snake Game with MPU6050 and OLED

Embedded Nerd's motion-controlled build: MPU6050, OLED and a complete Arduino sketch. The tutorial we picked for this swap, wired end to end.

**Source →** [embeddednerd.com](https://embeddednerd.com/esp32-snake-game-with-mpu6050-and-oled-display/?utm_source=rec&utm_campaign=issue-60)

### Tindie Blog

What makers actually sell: new gear, seller stories and open hardware news.

**Source →** [blog.tindie.com](https://blog.tindie.com/?utm_source=rec&utm_campaign=issue-60)

### Circuit Cellar

Embedded design articles from the magazine that has covered microcontrollers since 1988.

**Source →** [circuitcellar.com](https://circuitcellar.com/?utm_source=rec&utm_campaign=issue-60)

## From the bench

### Battery sizes for makers

One of 16 free no-signup bench tools for the projects in this issue.

**Source →** [link](/tools?utm_source=issue_page&utm_medium=bench&utm_campaign=issue-60)

---

Full issue: https://www.tinkernews.com/issues/60-pocket-reflex-iss-tracking-and-e-paper-adventures · Subscribe: https://www.tinkernews.com
