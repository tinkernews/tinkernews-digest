**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-11-03
**SUBJECT:** Episode Brief: TinkerNews Issue #60

Here is the detailed brief for our upcoming episode covering TinkerNews Issue #60. I've broken down every build with the key technical details and the "why makers care" angle for our audience. All information is directly from the source material.

---

### **Introduction**

This week's issue focuses on tangible, interactive builds. We see a lot of ESP32s being used for everything from games to home automation and even automotive hacking. Other themes include robotics, TinyML on the edge, and creative uses for Raspberry Pi boards.

---

### **Builds Covered in This Issue**

#### **Section: Arduino**

**1. Pocket Reflex Console With Three Games**
*   **What It Is:** A portable, self-contained gaming console for playing three different reflex-based games.
*   **How It Works Technically:** An ESP32-C3 microcontroller runs the game logic. It takes input from two physical buttons and provides feedback to the player using a round display and eight programmable RGB LEDs. The entire assembly is housed in a 3D-printed PLA enclosure.
*   **Standout Details:**
    *   **MCU:** ESP32-C3
    *   **Display:** Unspecified round display.
    *   **I/O:** Eight RGB LEDs, two pushbuttons.
    *   **Software:** Custom firmware with three games: Lightning Tap (reaction time), Chase the Light (tracking), and Duel Mode (two-player).
    *   **Construction:** The project guide covers breadboard prototyping, custom wiring, and a final PLA enclosure.
*   **Why a Maker Would Care:** This is a complete, polished project from start to finish. It's a great example of building a simple, dedicated device with a clear purpose, combining firmware, custom hardware, and a 3D-printed case.

**2. ESP32 Alarm Clock That Needs a Basket**
*   **What It Is:** An alarm clock that forces you to score a basket with a miniature basketball to silence the alarm.
*   **How It Works Technically:** An ESP32 controls a buzzer for the alarm sound. An infrared (IR) beam is positioned across the hoop. When the basketball passes through the hoop, it breaks the beam, which is detected by the ESP32 to turn off the alarm. The device uses BLE for initial setup.
*   **Standout Details:**
    *   **MCU:** ESP32
    *   **Sensor:** IR beam break sensor.
    *   **Output:** Buzzer.
    *   **Connectivity:** Bluetooth Low Energy (BLE).
    *   **Power:** Rechargeable battery.
    *   **Hardware:** Features a custom PCB and a 3D-printed mount.
*   **Why a Maker Would Care:** This project is a masterclass in the practical challenges of building an interactive device. It explicitly addresses real-world engineering problems like sensor alignment, managing timing and debounce for the IR sensor, ensuring proper antenna clearance for BLE on the custom PCB, and designing a functional enclosure.

**3. 8-Channel Arduino RC Link**
*   **What It Is:** A DIY radio control (RC) transmitter and receiver system capable of handling eight separate channels.
*   **How It Works Technically:** A transmitter unit built with an Arduino Nano reads analog and digital inputs from joysticks, potentiometers, and switches. This data is sent wirelessly via an nRF24L01 radio module to a receiver unit, also built with an Arduino Nano and nRF24L01. The receiver then generates corresponding PWM signals to drive servos or an Electronic Speed Controller (ESC).
*   **Standout Details:**
    *   **MCUs:** Two Arduino Nano boards (one for transmitter, one for receiver).
    *   **Radios:** Two nRF24L01 modules for 2.4 GHz communication.
    *   **Channels:** 8 channels.
    *   **Output:** PWM signals.
    *   **Construction:** Includes a hand-made enclosure and downloadable Arduino sketches.
*   **Why a Maker Would Care:** It demystifies RC systems by breaking them down into understandable components. The project is a starting point, intentionally leaving advanced topics like range testing, input calibration, failsafe programming, and interference mitigation for the builder to explore, making it a great learning platform.

**4. Scratch-Built RC Car Driven Over the Internet**
*   **What It Is:** A remote-controlled car that can be driven from anywhere in the world via the internet using a phone app.
*   **How It Works Technically:** An ESP-01 module on the car connects to a Wi-Fi network. It communicates with Google's Firebase real-time database. A phone app sends control commands (forward, back, left, right) to Firebase, which the ESP-01 reads and uses to control the car's drive motor and steering mechanism.
*   **Standout Details:**
    *   **MCU:** ESP-01 (a small ESP8266 module).
    *   **Drivetrain:** A salvaged gearbox and a main motor. The front wheel pivots are ingeniously made from pen refills.
    *   **Power:** 3S LiPo battery.
    *   **Connectivity:** Wi-Fi.
    *   **Software Stack:** Firebase for the cloud backend, and a custom phone app for control.
    *   **Chassis:** Hand-cut from PVC.
*   **Why a Maker Would Care:** This project demonstrates how to achieve "infinite range" for an RC vehicle by using a cloud service as an intermediary. It's also a great example of resourcefulness, using salvaged parts and common items like pen refills for mechanical components.

**5. Browser-Controlled 12-DOF Spider Robot**
*   **What It Is:** A four-legged spider robot with 12 degrees of freedom (DOF) that can be controlled from a web browser.
*   **How It Works Technically:** The robot uses a dual-controller setup. An ESP32-C3 acts as the web server, handling Wi-Fi commands from a browser interface. It then sends high-level commands to an Arduino Nano, which is responsible for the low-level motor control, managing the positions of the twelve servos, calculating foot positions, and executing the gait timing for walking, turning, and other movements.
*   **Standout Details:**
    *   **MCUs:** ESP32-C3 (for Wi-Fi/web server) and Arduino Nano (for servo control).
    *   **Actuators:** Twelve servos (3 per leg).
    *   **DOF:** 12.
    *   **Display:** An OLED screen is used for animated eyes and expressions.
    *   **Control:** A browser-based user interface.
*   **Why a Maker Would Care:** It showcases an effective distributed control architecture for complex robotics. By offloading the Wi-Fi and web server tasks to an ESP32, the Arduino Nano can focus entirely on the time-sensitive and processor-intensive job of precise servo control and kinematics, a common and powerful pattern in robotics.

**6. BLE Retail Display Timer and Tamper Alarm**
*   **What It Is:** A smart display stand for retail products that starts a timer when a product is lifted and sends tamper alerts via Bluetooth.
*   **How It Works Technically:** The system is built around an nRF52840 SoC running Zephyr RTOS. When a shopper lifts the product, a 90-second countdown begins. An internal sensor detects movement. If the device is moved or the product is not returned in time, an alarm sounds, and a BLE alert is sent to nearby staff phones. The system has a battery backup.
*   **Standout Details:**
    *   **MCU:** nRF52840.
    *   **OS:** Zephyr RTOS.
    *   **Connectivity:** Bluetooth Low Energy (BLE).
    *   **Features:** 90-second countdown timer, movement-based tamper alarm, battery backup.
    *   **Key Design Point:** Operates entirely locally, sending alerts directly to phones without needing store Wi-Fi or any cloud services.
*   **Why a Maker Would Care:** This is a professional-grade embedded systems project. It demonstrates how to build a reliable, low-power, standalone commercial device using an RTOS (Zephyr) and BLE for local communication, a valuable skill set for anyone looking to move from hobby projects to product development.

---

#### **Section: DIY Electronics**

**7. MatTris Arcade Packs Six Games Into 280 LEDs**
*   **What It Is:** A pocket-sized, custom-built arcade cabinet that plays six classic games on an RGB LED matrix.
*   **How It Works Technically:** An RP2040 Tiny microcontroller drives a 14x20 RGB LED matrix display. Six buttons provide user input for the games. The system is powered by a rechargeable battery and housed in a tinted acrylic case.
*   **Standout Details:**
    *   **MCU:** RP2040 Tiny.
    *   **Display:** 14x20 RGB LED matrix (280 total LEDs).
    *   **I/O:** Six buttons.
    *   **Hardware:** Custom PCB, rechargeable power circuit.
    *   **Games:** Tetris, Snake, Pong, Breakout, Car Dodge, and Space Invaders.
*   **Why a Maker Would Care:** It’s a beautifully integrated project that combines custom PCB design, a popular microcontroller (RP2040), and fun, classic game programming. It's a great inspiration for building a highly polished, portable electronic device.

---

#### **Section: ESP32**

**8. Draw Icons and Scroll Text with a MAX7219 Matrix**
*   **What It Is:** A tutorial on how to control single or chained 8x8 LED matrices using the MAX7219 driver chip.
*   **How It Works Technically:** An Arduino UNO (or ESP32) communicates with the MAX7219 chip via a 3-wire SPI protocol. The MD_MAX72XX library is used for drawing graphics (like icons) by controlling individual LEDs, while the MD_Parola library is used for creating scrolling text effects across multiple chained modules.
*   **Standout Details:**
    *   **Driver Chip:** MAX7219.
    *   **Display:** 8x8 LED matrix (single or chained).
    *   **Protocol:** SPI (3 control lines).
    *   **Software:** Arduino libraries MD_MAX72XX (graphics) and MD_Parola (text).
    *   **Hardware Note:** The guide warns that when using an ESP32 (a 3.3V device), level shifting is needed to interface with the 5V MAX7219, and that brightness should be kept low when powering from a computer's USB port.
*   **Why a Maker Would Care:** This is a foundational skill. MAX7219 matrices are a classic, inexpensive way to create displays. The tutorial breaks down how to use powerful libraries to go beyond just lighting up LEDs and create dynamic graphics and text, a key building block for many projects.

**9. An ESP32 Replaces the Leaf’s Cloud TCU**
*   **What It Is:** A replacement for the factory Telematics Control Unit (TCU) in a Nissan Leaf, designed to restore remote control functions after the official NissanConnect EV cloud service is shut down.
*   **How It Works Technically:** The device, named simppeliTCU, uses a LilyGO T-2CAN board, which combines an ESP32 with a CAN bus transceiver. It connects directly to the car's CAN bus. The custom firmware reads vehicle data and sends commands (for climate control, charging) over the bus. It provides local access via Wi-Fi and integrates with home automation systems via MQTT and Home Assistant.
*   **Standout Details:**
    *   **MCU/Board:** LilyGO T-2CAN (ESP32 with integrated CAN transceiver).
    *   **Protocol:** CAN bus for vehicle communication; Wi-Fi, MQTT for user access.
    *   **Software:** Custom ESP32-CAN firmware, integrates with Home Assistant.
    *   **Audience:** Explicitly noted as a draft for experienced builders due to the risks of vehicle wiring.
*   **Why a Maker Would Care:** This is an advanced "right to repair" style project. It shows how makers can reverse-engineer and replace cloud-dependent proprietary hardware to maintain functionality. It’s a deep dive into automotive hacking, CAN bus communication, and MQTT integration.

---

#### **Section: IoT**

**10. Arduino 4WD Robot With Wi-Fi Radar Mapping**
*   **What It Is:** A four-wheel-drive robot that autonomously maps its environment using an ultrasonic sensor and sends the map data to a web browser.
*   **How It Works Technically:** An Arduino UNO R4 WiFi controls the robot. Four TT motors provide mobility. A servo pans an HC-SR04 ultrasonic sensor back and forth to measure distances to obstacles. The Arduino collects this "radar" data and uses its built-in Wi-Fi to send it to a browser for rendering a 2D map, in a SLAM-like (Simultaneous Localization and Mapping) fashion.
*   **Standout Details:**
    *   **MCU:** Arduino UNO R4 WiFi.
    *   **Chassis:** 4WD with four TT motors.
    *   **Sensor:** HC-SR04 ultrasonic distance sensor mounted on a servo.
    *   **Power:** Uses separate batteries for the motors and the controller to prevent electrical noise issues.
    *   **Mapping:** The guide mentions floor markers for waypoint cues, but provides limited detail on the specific SLAM algorithm used.
*   **Why a Maker Would Care:** This is a great entry point into autonomous robotics and mapping. It combines motor control, sensor sweeps, and wireless data visualization in a single project. The separation of motor and logic power is a crucial, practical lesson for any robotics builder.

**11. ESP32 TinyML Vibration Monitor**
*   **What It Is:** A device that uses TinyML to monitor a machine for unusual vibrations that could indicate an impending fault.
*   **How It Works Technically:** An MPU6050 accelerometer measures the machine's vibrations. The ESP32 runs a locally trained TinyML model (a compact autoencoder) to analyze the vibration signature in real-time. The model learns the "normal" pattern of vibration. If a new vibration doesn't fit this pattern, it's flagged as an anomaly.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **Sensor:** MPU6050 (accelerometer/gyro).
    *   **Software Stack:** TinyML, specifically an autoencoder for anomaly detection.
    *   **Key Feature:** Does not require cloud processing or pre-labeled fault data. It performs all inference locally.
    *   **Output:** Onboard indicator, MQTT messages for alerts, and a browser dashboard for monitoring.
*   **Why a Maker Would Care:** This project makes predictive maintenance and on-device AI accessible. It's a fantastic real-world application of TinyML, showing how to detect problems without needing massive datasets or a cloud connection. It’s a big step beyond simple sensor-threshold projects.

**12. ESP32 Home Assistant Touchscreen Panel**
*   **What It Is:** A dedicated, wall-mountable touchscreen panel that acts as a simple, localized control interface for a Home Assistant smart home system.
*   **How It Works Technically:** An ESP32 with a connected touchscreen is flashed with custom firmware via a web browser. It connects to the local 2.4 GHz WiFi network and communicates with a Home Assistant instance. The display layout and controls (for lights, scenes, sensors, cameras, etc.) are configured from a web page.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **Display:** Touchscreen (unspecified model).
    *   **Connectivity:** 2.4 GHz WiFi.
    *   **Software:** Browser-based flashing; integrates directly with Home Assistant.
    *   **Function:** Provides a dedicated control point for a single room, capable of displaying sensor data, media controls, climate info, and more.
*   **Why a Maker Would Care:** It solves a common smart home problem: the need for a simple, dedicated interface that isn't a phone. It’s a great example of a practical home automation project that is highly customizable and bypasses the need for proprietary, expensive control panels.

**13. Gestire: An ESP32 Locker for Shared Lab Equipment**
*   **What It Is:** A smart locker system for managing shared equipment, like FPGA boards in a lab.
*   **How It Works Technically:** A user reserves equipment via a Flutter mobile app. A backend server running Flask with a SQLite database generates a six-digit PIN. The user enters this PIN on a keypad attached to the ESP32-controlled locker. The ESP32 validates the PIN, provides guidance on an LCD, and energizes a relay to unlock the correct compartment.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **I/O:** Keypad for input, LCD for output, relays for controlling locker doors.
    *   **Software Stack:** A full stack including a Flutter app (frontend), Flask and SQLite (backend), and C++/Arduino on the ESP32 (embedded).
*   **Why a Maker Would Care:** This is a complete IoT system architecture project. It covers everything from the embedded hardware to the mobile app and the web backend. The author also thoughtfully points out where it could be improved for a real-world installation (e.g., adding sensors to confirm equipment is present, better error recovery), which provides excellent learning points.

---

#### **Section: Raspberry Pi**

**14. Give a Raspberry Pi Pico Precise Stepper Motion**
*   **What It Is:** A tutorial on controlling a common 28BYJ-48 stepper motor with a Raspberry Pi Pico using MicroPython.
*   **How It Works Technically:** A Raspberry Pi Pico runs a MicroPython script. It sends step sequences to a ULN2003 driver board, which in turn powers the coils of the 28BYJ-48 stepper motor. A provided MicroPython library simplifies control with high-level commands for moving a specific number of steps, to a target angle, or in a set direction.
*   **Standout Details:**
    *   **MCU:** Raspberry Pi Pico.
    *   **Motor:** 28BYJ-48 geared stepper motor.
    *   **Driver:** ULN2003 board.
    *   **Software:** MicroPython with a custom library.
    *   **Key Considerations:** The guide notes the importance of using external power for the motor (not from the Pico) and the need for a home sensor in many real applications (sliders, gauges, etc.).
*   **Why a Maker Would Care:** This makes precise, repeatable motion control very approachable. The 28BYJ-48 is an extremely common and cheap stepper motor, and this tutorial provides the code and explanation to use it effectively with the popular Pico and MicroPython, opening the door to small robotics and automation projects.

**15. A Raspberry Pi Dish Tracks the ISS**
*   **What It Is:** A motorized dish antenna mount that automatically points at and tracks the International Space Station as it moves across the sky.
*   **How It Works Technically:** A Raspberry Pi Zero W acts as the brain. It runs software that fetches ISS pass predictions and orbital data from the internet, and also checks local cloud cover data to see if a pass will be visible. It then calculates the necessary azimuth and altitude angles in real-time and drives two stepper motors to position the dish accordingly.
*   **Standout Details:**
    *   **Controller:** Raspberry Pi Zero W.
    *   **Actuators:** Two stepper motors for azimuth and altitude control.
    *   **Data Sources:** Online APIs for orbital data, pass predictions, and cloud cover.
*   **Why a Maker Would Care:** This is a high "wow-factor" project that connects complex astronomical data to physical motion. It’s a fantastic example of a systems integration project, combining software (API calls, calculations), electronics (motor control), and mechanics to interact with the real world in a very visible and impressive way.

**16. InkQuest Puts Text Adventures on E-Paper**
*   **What It Is:** A handheld device with an e-paper screen that lets you play an interactive text adventure game generated by an AI.
*   **How It Works Technically:** An ESP32-C3 microcontroller manages the device. A rotary encoder is used for input. When the user makes a choice, the ESP32-C3 sends the last five turns of the story context to the Gemini AI model via an API call. Gemini returns four new choices, which the ESP32 then displays on the low-power e-paper screen.
*   **Standout Details:**
    *   **MCU:** ESP32-C3.
    *   **Display:** E-paper screen.
    *   **Input:** Rotary encoder with a push-button.
    *   **AI:** Uses the Gemini API for story generation.
    *   **Power:** Features a sleep mode and is estimated to have a 20-hour battery life.
    *   **Hardware:** Compact custom PCB and 3D printed case.
*   **Why a Maker Would Care:** It’s a novel use of three modern technologies: e-paper for a unique user experience, an ESP32 for low-power IoT connectivity, and a generative AI for dynamic content. It shows how to create a unique, portable device that wouldn't have been possible just a few years ago.

**17. Gemma 4 on a 4 GB Raspberry Pi 5**
*   **What It Is:** A guide explaining how to run the Gemma 4 E2B AI model locally and offline on a Raspberry Pi 5 with 4 GB of RAM.
*   **How It Works Technically:** The guide walks through setting up the necessary software (LiteRT) on a Raspberry Pi 5. LiteRT is used to run the Gemma 4 model, which consumes about 1.6 GB of RAM. The setup achieves an output speed of roughly 8 tokens per second without requiring any specialized AI hardware accelerator or a cloud connection.
*   **Standout Details:**
    *   **Hardware:** Raspberry Pi 5 with 4 GB of RAM.
    *   **AI Model:** Gemma 4 E2B.
    *   **Software:** LiteRT (an alternative to Ollama is also mentioned).
    *   **Performance:** Uses ~1.6 GB RAM, produces ~8 tokens/second.
    *   **Scope:** The guide covers all setup steps, including storage, cooling considerations, software downloads, and benchmarks.
*   **Why a Maker Would Care:** This demonstrates the increasing viability of running powerful AI models on affordable, single-board computers. It shows that makers can experiment with local, offline AI without needing expensive GPUs or cloud subscriptions, opening up possibilities for private, responsive AI-powered projects.

---

#### **Section: Robotics**

**18. ESP32 Board for a Robot Fox**
*   **What It Is:** A custom-designed ESP32-based controller board specifically for a 3D-printed quadruped (four-legged) robot fox.
*   **How It Works Technically:** This is a PCB design project. The board is centered around an ESP32 and provides all the necessary connections for the robot: ten servo headers for the leg joints, two DC motor connections, a TFT display connector, and various sensor inputs.
*   **Standout Details:**
    *   **MCU:** ESP32.
    *   **Outputs:** 10 servo connections, 2 DC motor connections.
    *   **I/O:** Connections for a TFT display and sensors.
    *   **Project Files:** The creator provides the schematic, Gerber files for PCB manufacturing, and a test sketch for an MPU6050.
*   **Why a Maker Would Care:** This is a great resource for anyone wanting to move beyond breadboards and design custom electronics for their robotics projects. By providing the full design files, it serves as an excellent template and learning tool for creating bespoke, integrated robot controller boards.