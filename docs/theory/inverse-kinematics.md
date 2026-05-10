# Inverse Kinematics — Theory & Mathematical Foundation

> Foundational mathematical documentation for the open-source quadruped robot project.

---

# Overview

This document contains the initial inverse kinematics derivations, geometric analysis, coordinate calculations, and motion-planning concepts explored during the early research phase of the quadruped robot.

The primary goal of this phase is to mathematically understand how a robotic leg can move to a desired coordinate position using:

- Coordinate geometry
- Trigonometry
- Triangle relationships
- Law of Cosines
- Joint angle calculations

The derivations and sketches documented here form the mathematical foundation for:

- Leg movement
- Walking gait generation
- Stability systems
- Coordinate-based control
- Future autonomous locomotion

---

# Core Objective

The purpose of inverse kinematics (IK) is to calculate the joint angles required to move the robotic leg endpoint to a target coordinate.

## Input

```text
Desired foot position → (x, y)
```

## Output

```text
Hip angle  → θ1
Knee angle → θ2
```

These calculations allow the quadruped robot to:

- Move legs precisely
- Control endpoint positioning
- Generate stable walking motion
- Maintain balance
- Execute coordinated gait movement

---

# Leg Model

The robotic leg is modeled as a:

```text
2-Link Planar Manipulator
```

## Leg Segments

| Variable | Description |
|---|---|
| `l1` | Upper leg length |
| `l2` | Lower leg length |
| `θ1` | Hip joint angle |
| `θ2` | Knee joint angle |
| `(x, y)` | Desired foot coordinate |

---

# Coordinate Geometry

The first step is determining the distance from the hip joint to the desired endpoint.

## Distance Formula

```text
r = √(x² + y²)
```

Where:

| Variable | Meaning |
|---|---|
| `r` | Distance from hip joint to foot |
| `x` | Horizontal displacement |
| `y` | Vertical displacement |

---

# Geometric Understanding

The robotic leg forms a triangle using:

- Upper leg link (`l1`)
- Lower leg link (`l2`)
- Endpoint distance (`r`)

The derivations rely on:

- Triangle decomposition
- Coordinate geometry
- Trigonometric identities
- Law of Cosines

---
