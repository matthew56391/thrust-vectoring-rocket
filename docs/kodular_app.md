# Kodular Android Control App

## Overview
An Android app built with Kodular for bench testing and manual control of the thrust-vectoring system over Bluetooth.

## Controls
- Single joystick: yaw and pitch control
- Slider: throttle control
- Buttons: connection and test actions

## Communication
- Bluetooth serial communication via HC-05
- Joystick X/Y values and throttle sent to Arduino Nano
- Input smoothing and dead zones handled primarily in firmware
