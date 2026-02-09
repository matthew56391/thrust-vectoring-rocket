# Firmware

Arduino-based firmware for a Bluetooth-controlled thrust-vectoring rocket test platform.

This firmware:
- Receives joystick + throttle commands over Bluetooth (HC-05 serial)
- Drives two servos (pitch + yaw) via PWM for gimbal vectoring
- Drives a brushless motor ESC via standard RC-style PWM (throttle)
- Applies dead zones / smoothing / safety limits in firmware (not the app)

---

## Files

- `rocket_control.ino` — main control firmware

---

## System Overview

**Inputs**
- Bluetooth serial commands from Android app (Kodular)

**Outputs**
- Servo PWM (pitch + yaw)
- ESC throttle PWM (brushless motor)

---

## Setup

### Requirements
- Arduino IDE (or PlatformIO)
- Arduino Nano/UNO
- HC-05 Bluetooth module

### Upload
1. Open `rocket_control.ino` in Arduino IDE  
2. Select **Board:** Arduino Nano/UNO 
3. Select correct **Port**  
4. Upload

---

## Notes

- Control smoothing and dead-zone behavior is implemented in firmware to keep the mobile app simple.
- This project was developed for bench testing and demonstration (not closed-loop flight control).

---

## Safety

- Remove propeller for initial software testing.
- Verify servo range limits before applying throttle.
- Use a secure test stand and keep clear of the propeller arc.
