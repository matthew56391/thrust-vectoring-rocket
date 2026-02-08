## Hardware Design Overview

This folder contains the complete hardware documentation for the thrust-vectoring rocket control system.  
It includes the electrical schematic, PCB fabrication files, and system-level wiring documentation.

The hardware was designed to interface an Arduino Nano with high-torque servos, an ESC, and a Bluetooth module, while allowing future expansion for inertial sensing.

---

## PCB Functionality

The custom PCB serves as a control and distribution board for:
- Arduino Nano power and signal breakout
- PWM control of yaw and pitch servos
- ESC throttle signal output
- Bluetooth (HC-05) serial communication
- Planned IMU integration (MPU-6050)
- Power decoupling and noise reduction

Power is supplied externally via a regulated 5V source.

---

## Files in This Folder

### `schematic.pdf`
Electrical schematic of the PCB showing:
- Signal routing
- Voltage divider for HC-05 RX (1kΩ / 2kΩ)
- Servo and ESC headers
- Power and ground distribution
- IMU header connections

This schematic represents the circuit implemented on the PCB.

---

### `system_wiring_diagram.png`
System-level wiring diagram showing how all components are connected in the full test setup, including:
- LiPo battery
- Buck converter
- Arduino Nano
- Servos
- ESC and motor
- Bluetooth module

This diagram is intended for real-world assembly and troubleshooting.

---

### `pcb_2d.png`
2D PCB layout view showing:
- Component placement
- Copper routing
- Power trace widths
- Connector orientation

---

### `pcb_3d.png`
3D render of the PCB used to visualize:
- Board form factor
- Header placement
- Mechanical clearances

---

### `gerbers.zip`
Manufacturing files (Gerbers) generated for PCB fabrication.

---

## Notes
- This hardware was designed for **bench testing only**
- No free-flight operation was performed

