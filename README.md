# Line Following Robot using Arduino Nano

![Line Following Robot](robot.png)

## Project Overview
This project is a two-wheeled line-following robot built using an Arduino Nano. The robot is designed to autonomously follow a predefined black line on a white surface using an infrared (IR) sensor.

## Description
The robot uses a single IR sensor to detect the contrast between black and white surfaces. Based on the sensor input, the Arduino controls the left and right motors to continuously adjust direction. This creates a simple but effective feedback system for line tracking.

## Hardware & Tools
- Microcontroller: Arduino Nano  
- Sensor: IR line detection sensor  
- Motors: 2 DC motors (differential drive)  
- Chassis: Two-wheel base with front support roller  
- Programming Language: Arduino (C/C++)  
- Power Supply: Battery  
- Tools: Arduino IDE  

## Working Principle
- The IR sensor detects the surface color (black or white)
- If black is detected → the robot turns in one direction  
- If white is detected → the robot turns in the opposite direction  
- Continuous switching between left and right creates path tracking  
- Motor speed is controlled using PWM signals  

## My Contribution
- Designed and assembled the robot hardware  
- Positioned and calibrated the IR sensor for accurate detection  
- Implemented motor control using PWM signals  
- Programmed the Arduino Nano in C/C++  
- Tested and optimized the robot for stable movement on curved paths  

## Features
- Real-time line detection using IR sensor  
- Differential motor control for direction correction  
- Adjustable motor speed  
- Continuous path tracking on curved lines  
- Simple and efficient control logic  

## Design Insights
- Sensor placement close to the ground improves detection accuracy  
- A front support roller helps maintain stability and alignment  
- Motor speed must be limited to match sensor response time  
- High speed can cause overshooting and unstable tracking  
- System performance depends on balancing speed and control  

## Results
The robot successfully follows curved (snake-like) paths with stable tracking.  
Minor oscillations occur due to continuous correction, but overall movement remains accurate and reliable.

## Learning Outcomes
- Understanding of line-following control logic  
- Practical use of IR sensors in embedded systems  
- Implementation of PWM-based motor control  
- Experience in hardware-software integration  
- Awareness of real-world limitations (sensor vs speed trade-off)  

## Repository Structure
```text
line-following-robot-arduino/
├── code/
│   └── line_following_robot.ino
├── robot.png
└── README.md
