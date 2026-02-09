# Bill of Materials (BOM)

This document lists the primary components used in the rocket thrust-vectoring
control system, organized by subsystem.

---

## Control & Communication

| Component | Part / Spec | Purpose |
|---------|-------------|---------|
| Microcontroller | Arduino Nano | Central control |
| Bluetooth Module | HC-05 | Wireless serial communication |
| USB Interface | Mini-USB (Nano) | Programming & debugging |

---

## Actuation

| Component | Part / Spec | Purpose |
|---------|-------------|---------|
| Servo Motor (Yaw) | MG996R | Yaw-axis thrust vectoring |
| Servo Motor (Pitch) | MG996R | Pitch-axis thrust vectoring |
| Brushless Motor | RS2205 2300KV | Thrust generation |
| ESC | 30A Brushless ESC | Motor speed control |

---

## Power

| Component | Part / Spec | Purpose |
|---------|-------------|---------|
| Battery | 3S 11.1V LiPo | Primary power source |
| Buck Converter | XL4015 | Step-down to 5V |
| Capacitors | Electrolytic | Power filtering & noise suppression |

---

## Mechanical

| Component | Part / Spec | Purpose |
|---------|-------------|---------|
| Ball Bearing | 608ZZ | Gimbal support |
| Fasteners | M3 screws & nuts | Structural mounting |
| Structural Parts | PLA / PLA+ (3D Printed) | Frame & mounts |
