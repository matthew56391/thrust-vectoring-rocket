# Thrust-Vectoring Rocket Test Rig

## Overview
This project is a bench-tested thrust-vectoring rocket system designed to explore mechanical gimbal design, embedded control, and power electronics integration. The system uses a 2-axis gimbal driven by high-torque servos to redirect thrust from a brushless motor, controlled by an Arduino-based system with Bluetooth input.

This project was developed as a personal engineering project and is intended for **ground testing only**.

---

## Key Features
- 2-axis thrust-vectoring gimbal (yaw + pitch)
- Custom-designed PCB for control and power distribution
- Arduino Nano–based firmware
- Bluetooth control via HC-05 module
- Brushless motor + ESC thrust control
- 3D-printed structural components
- Modular design for future sensor-based stabilization (IMU)

---

## System Architecture
**Power**
- 3S LiPo battery
- Buck converter stepping down to 5V for logic and servos
- ESC powering brushless motor

**Control**
- Arduino Nano
- PWM control of servos and ESC
- Bluetooth serial input for joystick commands

---

## Repository Contents

/firmware - Arduino control code
/hardware - PCB schematic, gerbers, and BOM
/stl - 3D printable parts
/images - Project photos
/docs - Wiring diagrams and assembly notes

---

## Safety Notice
⚠️ **This project is for bench testing only.**  
No free-flight testing was performed. Always remove propellers during setup and follow LiPo battery safety procedures.

---

## Future Work
- IMU-based stabilization (MPU-6050)
- Control loop refinement
- Improved power filtering and PCB revision

---

## Author
Matthew Cuebas  
Electrical Engineering – University of Texas at San Antonio
