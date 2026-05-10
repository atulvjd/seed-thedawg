# Quadruped Robot Architecture

## Overview

This project is an open-source quadruped robot designed using affordable off-the-shelf components. The robot is being developed with a strong focus on modularity, accessibility, reproducibility, and detailed engineering documentation.

The architecture is designed to allow incremental development, testing, and future scalability.

---

# System Goals

- Stable quadruped locomotion
- Modular mechanical structure
- Affordable hardware design
- Beginner-friendly development
- Expandable software architecture
- Open-source documentation

---

# Mechanical Architecture

## Leg Design
- 2 DOF per leg
- Servo-actuated joints
- Modular leg structure
- 3D printable components

## Body Structure
- Centralized electronics mounting
- Lightweight frame design
- Symmetrical leg placement

## Materials
- PLA/PETG for prototyping
- Metal reinforcement possible in future versions

---

# Electronics Architecture

## Main Controller
- ESP32 Development Board

Purpose:
- Servo control
- Communication handling
- Motion logic execution

---

## Servo Control System

Component:
- PCA9685 Servo Driver

Purpose:
- Stable PWM generation
- Multi-servo management

---

## Power System

Components:
- 2S Li-ion/LiPo Battery
- DC-DC Buck Converter

Purpose:
- Stable voltage regulation
- Servo power delivery
- Electronics protection

---

# Software Architecture

## Motion Layer
Handles:
- Servo movement
- Joint angle control
- PWM signal generation

---

## Kinematics Layer
Handles:
- Inverse kinematics
- Coordinate calculations
- Leg positioning

---

## Gait Layer
Handles:
- Walking patterns
- Leg synchronization
- Stability control

---

## Future Expansion Layer
Planned future systems:
- Computer vision
- Autonomous navigation
- Sensor fusion
- AI-assisted movement

---

# Development Strategy

The robot will be developed incrementally:

1. Servo testing
2. Single joint movement
3. Single leg prototype
4. Inverse kinematics implementation
5. Standing balance
6. Walking gait generation
7. Full quadruped integration

---

# Current Development Focus

Current priority:
- Hardware research
- System architecture
- Inverse kinematics documentation
- Servo testing preparation

The first physical milestone is achieving stable movement of a single robotic leg.