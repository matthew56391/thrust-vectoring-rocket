# Thrust-Vectoring Rocket Test Rig

## Overview
This project is a bench-tested thrust-vectoring rocket control system built to explore mechanical gimbal design, embedded control, and power electronics integration.

At its core is a 2-axis gimbal (yaw and pitch) driven by high-torque servos that redirects thrust from a brushless motor. The system is controlled by an Arduino Nano and operated wirelessly through a custom Bluetooth interface.

This was developed as a personal engineering project focused on hands-on system integration and rapid prototyping.

This project was developed as a personal engineering project and is intended for
**ground testing only**.

---

## Key Features
- 2-axis thrust-vectoring gimbal (yaw + pitch)
- Custom-designed PCB for control and power distribution
- Arduino Nano firmware for real-time control
- Bluetooth control via HC-05
- Brushless motor + ESC thrust control
- 3D-printed structural and mounting components
- Modular architecture designed for future IMU-based stabilization
- Custom Android control app built in Kodular

Demonstration videos show live gimbal articulation and thrust response under bench testing conditions.

---

## System Architecture

### Power
- 3S LiPo battery
- Buck converter stepping down to regulated 5V for logic and servos
- ESC powering the brushless motor
- Dedicated power routing through a custom PCB

### Control
- Arduino Nano as primary controller
- PWM control of servos and ESC
- Bluetooth serial input for joystick commands
- Android control app with joystick, throttle slider, and buttons

---

## System Overview (Images)
Project photos showing the gimbal assembly, internal electronics, and test setup
are available in the [`/images`](images) directory.

---

## Demonstration Videos
Demonstration and walkthrough videos are documented in the
[`/videos`](videos) folder, including:
- Real-time gimbal and thrust control demonstration
- Integrated rocket system overview
- Detailed gimbal and electronics walkthrough
- Bench testing under load

---

## Bill of Materials (BOM)
A complete, subsystem-organized Bill of Materials is available here:  
📄 [`hardware/bill_of_materials.md`](hardware/bill_of_materials.md)

*The BOM focuses on system-critical components rather than manufacturing
consumables.*

---

## Control App (Kodular)
A custom Android control app was developed using **Kodular** to support real-time
manual control during bench testing. The app provides:
- A single joystick for yaw and pitch control
- A throttle slider for motor speed
- Buttons for connection and testing actions

Joystick X/Y values and throttle commands are transmitted over Bluetooth (HC-05)
to the Arduino Nano, where firmware maps inputs to servo angles and ESC throttle
via PWM.

Kodular was selected to enable rapid prototyping of the control interface while
keeping control logic centralized in firmware.

Additional documentation:  
📄 [`docs/kodular_app.md`](docs/kodular_app.md)

---

## Repository Structure
- `/firmware` – Arduino control firmware
- `/hardware` – PCB schematic, Gerbers, and wiring documentation
- `/stl` – 3D-printable mechanical components
- `/images` – Project and test photos
- `/videos` – Linked demonstration and walkthrough videos
- `/docs` – Supporting documentation

---

## Safety Notice
⚠️ **This project is for bench testing only.**  
No free-flight testing was performed. Always remove propellers during software
setup and follow proper LiPo battery safety procedures.

---

## Future Work
- IMU-based stabilization (MPU-6050)
- Control loop refinement
- Improved power filtering and PCB revision

---

## Author
Matthew Cuebas  
Electrical Engineering – University of Texas at San Antonio
