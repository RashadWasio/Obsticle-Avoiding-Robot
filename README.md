# Obstacle Avoiding Robot (Arduino-Based)

## Overview
This project demonstrates the design and implementation of an autonomous obstacle avoiding robot using an Arduino platform. The system integrates multiple sensors and actuators to enable real-time environment perception and intelligent navigation without human intervention.

The robot continuously evaluates its surroundings, detects obstacles, and dynamically selects the safest path to avoid collisions. This project provides a solid foundation for beginners in robotics, embedded systems, and autonomous control.

## Key Features
* Fully autonomous navigation
* Dual-sensor obstacle detection (Ultrasonic and IR)
* Servo-based directional scanning
* Intelligent path selection algorithm
* Recovery mechanism for confined spaces
* Modular and maintainable code structure

## Hardware Components
* Arduino Uno
* L293D Motor Driver Shield
* DC Gear Motors (N20 recommended)
* Ultrasonic Sensor (HC-SR04)
* IR Obstacle Sensor
* Servo Motor (SG90 or equivalent)
* Power Source (18650 Li-ion battery or equivalent)
* Chassis, wheels, and supporting hardware

## System Architecture
The robot operates using a layered decision-making approach:
1. Sensing Layer

   * Ultrasonic sensor measures distance to obstacles
   * IR sensor detects close-range objects

2. Processing Layer

   * Arduino processes sensor data in real time
   * Decision logic determines movement behavior

3. Actuation Layer

   * Motor shield controls DC motors
   * Servo motor adjusts sensor direction for scanning

## Operational Workflow
* The robot moves forward when no obstacle is detected
* When an obstacle is detected within a defined threshold:

  * The robot stops and reverses slightly
  * Performs directional scanning (left and right)
  * Compares distances and selects the optimal path
* If both directions are blocked, an alternating escape strategy is applied

## Pin Configuration
| Component       | Arduino Pin           |
| --------------- | --------------------- |
| Ultrasonic TRIG | A1                    |
| Ultrasonic ECHO | A2                    |
| IR Sensor       | A0                    |
| Servo Motor     | D10                   |
| Motors          | L293D Shield (M1, M2) |

## Configuration Parameters
Key parameters can be adjusted directly in the code:
* Motor speed (drive and turning)
* Distance thresholds for detection
* Servo angles for scanning
* Timing delays for movement and scanning

## Learning Outcomes
* Embedded system design using Arduino
* Sensor integration and signal processing
* Motor control using driver modules
* Implementation of basic autonomous navigation logic

## Future Enhancements
* Replace blocking delays with non-blocking timing (millis)
* Integrate wireless control (Bluetooth or Wi-Fi)
* Add line-following capability
* Upgrade motor driver (e.g., TB6612FNG)
* Incorporate vision-based or AI-based navigation

## Author
Rashad Wasio
CSE Student | Robotics Enthusiast
