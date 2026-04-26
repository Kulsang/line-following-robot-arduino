# Line Following Robot using Arduino Nano

## Project Overview

![Line Following Robot](robot.png)

---

## Description
This project is a two-wheeled line-following robot built using an Arduino Nano. The robot follows a predefined black path on a white surface using an infrared (IR) sensor.

The sensor is positioned very close to the ground to improve detection accuracy. The robot continuously adjusts its direction using differential motor control.

---

## Features
- Line detection using IR sensor  
- Differential motor control (left/right correction)  
- Real-time path tracking  
- Adjustable motor speed  
- Continuous navigation on curved paths  

---

## Hardware & Tools
- Microcontroller: Arduino Nano  
- Sensor: IR line detection sensor  
- Motors: DC motors (2-wheel drive)  
- Chassis: Two-wheel base with front support roller  
- Programming Language: Arduino (C/C++)  
- Power Supply: Battery  

---

## Working Principle
- The IR sensor detects whether the surface is black or white  
- If black is detected → one motor rotates  
- If white is detected → the other motor rotates  
- This creates continuous left-right correction  
- The robot follows the line through rapid directional adjustments  

---

## Arduino Code

```cpp
#define IR_SENSOR 2

#define LEFT_MOTOR_PIN 5
#define RIGHT_MOTOR_PIN 6

#define MOTOR_SPEED 120

void setup() {
  pinMode(IR_SENSOR, INPUT);
  pinMode(LEFT_MOTOR_PIN, OUTPUT);
  pinMode(RIGHT_MOTOR_PIN, OUTPUT);
}

void loop() {
  int sensorValue = digitalRead(IR_SENSOR);

  if (sensorValue == LOW) {
    // Black detected
    analogWrite(LEFT_MOTOR_PIN, MOTOR_SPEED);
    analogWrite(RIGHT_MOTOR_PIN, 0);
  } 
  else {
    // White detected
    analogWrite(LEFT_MOTOR_PIN, 0);
    analogWrite(RIGHT_MOTOR_PIN, MOTOR_SPEED);
  }
}
