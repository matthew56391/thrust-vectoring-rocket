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
- Custom Android control app (Kodular) with joystick, slider, and buttons

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
- Custom Android control app (Kodular) with joystick, throttle slider, and buttons

---

## System Overview (Images)
*Images of the gimbal assembly, PCB, and test rig will be added here.*

## Demonstration Videos
*Short demonstration videos showing gimbal actuation and control response will be added here.*

---

## Bill of Materials (BOM)

### Control & Communication

| Component | Part / Spec | Purpose |
|---------|------------|--------|
| Microcontroller | Arduino Nano | Central control |
| Bluetooth Module | HC-05 | Wireless serial communication |
| USB Interface | Mini-USB (Nano) | Programming & debug |

### Actuation

| Component | Part / Spec | Purpose |
|---------|------------|--------|
| Servo Motor (Yaw) | MG996R | Yaw-axis thrust vectoring |
| Servo Motor (Pitch) | MG996R | Pitch-axis thrust vectoring |
| Brushless Motor | RS2205 2300KV | Thrust generation |
| ESC | 30A Brushless ESC | Motor speed control |

### Power

| Component | Part / Spec | Purpose |
|---------|------------|--------|
| Battery | 3S 11.1V LiPo | Primary power source |
| Buck Converter | XL4015 | Step-down to 5V |
| Capacitors | Electrolytic + ceramic | Power filtering & noise suppression |

### Mechanical

| Component | Part / Spec | Purpose |
|---------|------------|--------|
| Ball Bearing | 608ZZ | Gimbal support |
| Fasteners | M3 screws & nuts | Structural mounting |
| Structural Parts | PLA / PLA+ 3D prints | Frame & mounts |

*Note: This BOM lists system-critical components rather than manufacturing consumables.*

---

## Control App (Kodular)

A custom Android control app was developed using **Kodular** to provide real-time manual control during bench testing. The app includes a single on-screen joystick for yaw and pitch control, a slider for throttle input, and additional buttons for connection and testing.

The app sends joystick X/Y values and throttle commands to the Arduino Nano over Bluetooth (HC-05), where the firmware maps inputs to servo angles and ESC throttle using PWM control.

**Why Kodular:** It enabled rapid prototyping of the control interface, allowing quick iteration on input scaling and responsiveness without slowing down hardware development.

Additional details: [`docs/kodular-app.md`](docs/kodular-app.md)

*Note: The mobile app is a lightweight test interface used for ground testing and validation, not the primary focus of the project.*

---

## Repository Contents
- `/firmware` – Arduino control code  
- `/hardware` – PCB schematic and gerber files  
- `/stl` – 3D printable parts  
- `/images` – Project photos  
- `/docs` – Wiring diagrams and assembly notes  

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
