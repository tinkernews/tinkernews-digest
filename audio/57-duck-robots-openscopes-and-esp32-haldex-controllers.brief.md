**TO:** Podcast Hosts
**FROM:** Research Editor
**DATE:** 2026-10-12
**SUBJECT:** Episode Brief: TinkerNews #57 - Duck Robots, OpenScopes, and ESP32 Haldex Controllers

Here is the detailed brief for our upcoming episode covering TinkerNews Issue #57. I've broken down every build project with the key technical details and the "why it matters" angle for our maker audience. Please stick to these facts sourced directly from the newsletter.

---

### **Episode Brief: TinkerNews #57**

#### **1. Printable Duck Robot (XGO-Duck)**

*   **What It Is:** An open-hardware, 3D-printable, bipedal robot shaped like a duck, designed for motion experiments.
*   **How It Works Technically:** The robot is built from printed parts and actuated by fifteen serial servos. A central controller board is wired to all servos to coordinate movement. The project includes a browser-based interface for calibrating the servos and controlling the robot. It is intended as a platform for reinforcement-learning experiments to develop behaviors like balancing and walking.
*   **Standout Details:**
    *   **Part Count:** Fifteen serial servos.
    *   **Architecture:** Open hardware project.
    *   **Software Stack:** Utilizes a browser-based calibration tool and is designed for reinforcement-learning experiments.
*   **Why a Maker Cares:** This is a complex robotics project that goes beyond a simple wheeled rover. It’s an accessible platform for makers interested in bipedal locomotion, multi-servo coordination, and applying machine learning (specifically reinforcement learning) to a physical robot.

#### **2. OpenScope Firmware for FNIRSI 2C53T**

*   **What It Is:** A complete, custom, open-source firmware replacement for the factory software on the FNIRSI 2C53T, a specific model of digital oscilloscope.
*   **How It Works Technically:** The firmware was developed by reverse-engineering the device's hardware. The new software directly initializes and controls the AT32 microcontroller and configures the Gowin FPGA. It then captures signals from the scope's probes and renders them as live waveforms on the screen, replacing the buggy original firmware. Flashing this firmware is high-risk and can result in lost calibration data or a bricked device.
*   **Standout Details:**
    *   **Target Hardware:** FNIRSI 2C53T Oscilloscope.
    *   **Chips:** AT32 microcontroller, Gowin FPGA.
    *   **Process:** Built from scratch via reverse engineering.
*   **Why a Maker Cares:** This is a masterclass in reclaiming and improving commercial hardware. It shows how a maker can take a functional but flawed tool and, through deep technical effort, replace its core software to fix bugs and gain control. It's a high-stakes project that highlights the power of open-source reverse engineering.

#### **3. ESP32-S3 Haldex Controller (OpenHaldex-S3)**

*   **What It Is:** A DIY controller that replaces or augments the factory controller for Haldex all-wheel-drive systems found in VAG (Volkswagen Auto Group) vehicles.
*   **How It Works Technically:** The system uses an ESP32-S3 microcontroller board running custom firmware, connected to the vehicle via an inline wiring harness. This allows it to interact with the Haldex system. It hosts a web server, providing a browser-based interface for diagnostics, data logging, and performance tuning.
*   **Standout Details:**
    *   **Chip:** ESP32-S3.
    *   **Software:** MIT-licensed public firmware.
    *   **Interface:** Browser-based setup and control.
    *   **Note:** This open project is distinct from the newer, proprietary "OpenHaldex SS" application.
*   **Why a Maker Cares:** This project takes the ESP32 out of the lab and puts it into a demanding automotive application. For makers who are also car enthusiasts, it provides an open-source path to inspect and tune a complex, proprietary vehicle system, which is normally a black box.

#### **4. ROS 2 Rover Electronics (Linorobot2)**

*   **What It Is:** Firmware and electronics guidance for building the hardware base of a mobile robot that integrates with ROS 2 (Robot Operating System 2).
*   **How It Works Technically:** It uses either an ESP32 or a Raspberry Pi Pico to handle the low-level tasks of motor control and odometry (tracking wheel movement). This microcontroller then communicates with the main ROS 2 system, providing the essential link between the high-level robotics software and the physical hardware.
*   **Standout Details:**
    *   **Chips:** Supports ESP32 or Raspberry Pi Pico.
    *   **Software Stack:** Firmware integrates directly with ROS 2.
    *   **Protocols:** Supports USB or Wi-Fi for communication.
    *   **Features:** Includes Over-the-Air (OTA) update capability and network diagnostics.
*   **Why a Maker Cares:** It provides a crucial bridge between simple microcontroller projects and the powerful, industry-standard ROS 2 ecosystem. Makers can use familiar, low-cost boards (Pico, ESP32) to build the foundation for a serious autonomous robot without having to develop the complex ROS 2 hardware interface from scratch.

#### **5. Arduino Metal Detector**

*   **What It Is:** A DIY metal detector that can distinguish between target types and estimate their depth.
*   **How It Works Technically:** The sensor is a hand-wound coil that is part of a paired oscillator circuit. The presence of metal near the coil causes a small frequency shift in the oscillators. An Arduino measures this shift to detect metal. The project's software analyzes the signal to classify targets as likely ferrous or non-ferrous and estimates depth in zones.
*   **Standout Details:**
    *   **Core Components:** Arduino, hand-wound coil, paired oscillators.
    *   **User Interface:** An LCD screen displays calibration data and detection results.
    *   **Features:** Provides target classification (ferrous vs. non-ferrous) and depth estimation.
*   **Why a Maker Cares:** This is a classic electronics project that demonstrates sensitive analog measurement with a microcontroller. It combines coil winding, oscillator theory, and signal processing on an Arduino to create a genuinely useful tool, showing how basic components can be used for sophisticated sensing.

#### **6. Home Assistant Touch Panels (Tessera)**

*   **What It Is:** A system for turning low-cost ESP32-based color touchscreen displays into dedicated, room-specific control panels for a Home Assistant smart home.
*   **How It Works Technically:** The project uses a Home Assistant add-on called "Screen Manager" to design a shared dashboard layout. This dashboard is then deployed to multiple supported ESP32 touchscreen devices over the network. Each panel can display and control lights, climate, media, locks, and other Home Assistant entities.
*   **Standout Details:**
    *   **Platform:** ESP32-based color touchscreens.
    *   **Software:** Requires a "Screen Manager" add-on for Home Assistant.
    *   **Functionality:** Centralized design of a shared dashboard, deployed to multiple devices.
*   **Why a Maker Cares:** It’s a very practical and polished smart home project. It solves a real-world problem—the need for dedicated, local interfaces—using affordable and accessible ESP32 hardware, without requiring complex custom firmware for each individual panel.

#### **7. GeekMagic SmallTV Mod**

*   **What It Is:** A replacement firmware for the GeekMagic SmallTV, a small desktop device with a color screen, turning it into a customizable Wi-Fi dashboard.
*   **How It Works Technically:** The stock software on the device is completely replaced. The new, custom firmware connects to Wi-Fi and uses a web interface for configuration, mode selection, and wireless updates. The single codebase supports several ESP variants. It can be configured to display stock prices, Claude API usage, or nearby aircraft data.
*   **Standout Details:**
    *   **Target Hardware:** GeekMagic SmallTV.
    *   **Chip:** Supports several ESP variants.
    *   **Interface:** Web interface for settings and OTA updates.
    *   **Features:** Displays stock prices, Claude usage, and aircraft data.
*   **Why a Maker Cares:** Similar to the OpenScope project, this is about taking an existing commercial product and repurposing it completely with custom firmware. It turns a novelty gadget into a practical, personalized information display, showcasing a clean and compact firmware project.

#### **8. Waveshare Industrial I/O Network Controller**

*   **What It Is:** Open-source firmware that turns a Waveshare ESP32-S3 industrial I/O board into a versatile network-connected controller.
*   **How It Works Technically:** The firmware runs on the Waveshare board and leverages its hardware features (isolated I/O, Ethernet). It adds support for multiple communication protocols including MQTT, Modbus RTU, and CAN bus. It also includes a web interface for settings and can run local automation rules written in JavaScript. Different protocols are handled by separate applications to manage memory.
*   **Standout Details:**
    *   **Target Hardware:** Waveshare ESP32-S3-based industrial I/O boards.
    *   **Hardware Features:** 8 isolated inputs, 8 outputs, Ethernet, Power over Ethernet (PoE).
    *   **Protocols:** MQTT, Modbus RTU, CAN bus.
    *   **Software:** Web settings, local JavaScript rules, optional Matter build.
*   **Why a Maker Cares:** This project elevates the ESP32 from a hobbyist board to a robust industrial controller. It provides the open-source software to take advantage of rugged, off-the-shelf hardware, making it suitable for serious automation, home control, or workshop tasks that require more resilience than a standard dev kit.

#### **9. Low Cost Solar Car**

*   **What It Is:** A very simple, lightweight car powered directly by a small solar panel.
*   **How It Works Technically:** A small photovoltaic panel is connected directly to a DC motor. When sunlight hits the panel, it generates a current that drives the motor, which in turn moves the car. There are no batteries or complex control electronics mentioned.
*   **Standout Details:**
    *   **Parts:** Small photovoltaic panel, DC motor, lightweight chassis components.
    *   **Circuit:** Direct connection from panel to motor.
*   **Why a Maker Cares:** It's an excellent entry-level project for demonstrating fundamental concepts of solar power and basic physics. It serves as a tangible, hands-on test platform for experiments with photovoltaics, panel angles, gearing, and friction, making it great for science fairs or educational purposes.

#### **10. ESP32-C6 RMT LED Driver**

*   **What It Is:** A demonstration of how to reliably control a WS2812 addressable LED using a specific hardware peripheral on the ESP32-C6.
*   **How It Works Technically:** It uses the ESP32-C6's RMT (Remote Control) peripheral to generate the precise, sub-microsecond timing required by the WS2812 protocol. The RMT hardware handles the signal generation, ensuring the timing remains stable even while the main CPU is busy with other tasks like FreeRTOS and wireless network handlers. The project outputs the frame timing to the serial console for verification.
*   **Standout Details:**
    *   **Chip:** ESP32-C6 (on a C6-DevKitC-1 board).
    *   **Component:** Onboard WS2812 LED.
    *   **Technology:** Uses the RMT peripheral for hardware-based signal generation.
*   **Why a Maker Cares:** This addresses a common problem: bit-banged protocols like the WS2812's can be unreliable on microcontrollers running an RTOS or complex network stacks. Using a dedicated hardware peripheral like the RMT is the "correct" and robust way to solve this, and this project is a practical example of how to do it.

#### **11. Open Source Robot Vacuum (OOMWOO)**

*   **What It Is:** A work-in-progress project to build a robot vacuum from affordable, replaceable parts for around $200.
*   **How It Works Technically:** The design is modular, breaking the vacuum into separate components: drive modules, a caster, suction hardware, and sensors. A Raspberry Pi is used for the main control board. The project is still in development, with final performance dependent on the integration of mechanical parts, electronics, and software.
*   **Standout Details:**
    *   **Control:** Raspberry Pi.
    *   **Cost Target:** Approximately $200.
    *   **Design:** Modular and composed of replaceable parts.
    *   **Status:** Work in progress.
*   **Why a Maker Cares:** This project aims to "open-source" a complex consumer appliance. It's ambitious, and its modular approach could make repair and modification much easier than with a commercial unit. It represents the challenge of matching the navigation and cleaning performance of commercial products with DIY hardware and software.