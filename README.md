# line-following-robot-arduino
Two-wheeled line following robot using Arduino Nano and IR sensor with differential motor control

## Description
This project is a two-wheeled line-following robot built using Arduino Nano. The robot follows a predefined black line on a white surface using an infrared (IR) sensor.

The system uses differential motor control to continuously adjust direction and maintain alignment with the path.

---

## Features
- Line detection using IR sensor
- Differential motor control for steering
- Real-time left-right correction
- Adjustable motor speed
- Continuous path tracking

---

## Hardware & Tools
- Microcontroller: Arduino Nano
- Sensor: IR line detection sensor
- Motor Driver: L298N (if used, otherwise remove)
- Motors: DC motors (2 wheels)
- Programming Language: Arduino (C/C++)
- Power Supply: Battery

---

## Working Principle
- The IR sensor detects surface color (black or white)
- If black is detected → one motor activates
- If white is detected → the other motor activates
- This creates continuous left-right correction
- The robot follows the path using rapid adjustments

---

## Challenges & Learning
- Sensor placement was critical for accurate detection
- Speed had to be limited due to sensor response time
- High speed caused overshooting of the line
- Learned trade-off between speed and accuracy

---

## Result
The robot successfully follows a curved (snake-like) path with stable tracking and minor oscillations.

---

## Author
Kulsang Thupten Sherpa  
Electrical Engineering Student (RWU, Germany)
