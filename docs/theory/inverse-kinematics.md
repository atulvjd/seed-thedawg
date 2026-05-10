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

# Law of Cosines Derivation

## Initial Equation

```text
r² = l1² + l2² - 2l1l2cos(α)
```

Where:

```text
α = π - θ2
```

Using:

```text
cos(π - θ2) = -cos(θ2)
```

The equation becomes:

```text
x² + y² = l1² + l2² + 2l1l2cos(θ2)
```

---

# Knee Joint Angle Equation

Rearranging the equation:

```text
cos(θ2) = (x² + y² - l1² - l2²) / (2l1l2)
```

## Final Knee Angle Formula

```text
θ2 = cos⁻¹((x² + y² - l1² - l2²) / (2l1l2))
```

This equation calculates the knee joint angle required to place the robotic foot at a target coordinate.

---

# Hip Joint Angle Equation

The hip angle is calculated using two trigonometric components.

## Final Hip Angle Formula

```text
θ1 = tan⁻¹(y/x) - tan⁻¹((l2sinθ2)/(l1 + l2cosθ2))
```

This determines the orientation of the upper leg relative to the robot body.

---

# Workspace Analysis

The calculations show that the robotic leg has a limited reachable workspace.

## Reachability Condition

```text
|l1 - l2| ≤ r ≤ l1 + l2
```

This determines whether a target coordinate is physically reachable.

## Workspace Considerations

- Joint angle limits
- Servo rotation constraints
- Mechanical collisions
- Stability boundaries
- Maximum extension limits

---


# Mechanical Observations

The early calculations and sketches highlight several important design insights.

## Important Engineering Factors

- Servo placement affects torque distribution
- Longer links increase reach but reduce stability
- Weight distribution impacts balancing
- Joint rigidity affects smoothness
- Link dimensions influence walking efficiency
- Mechanical constraints affect gait planning

---

# Development Strategy

The mathematical and architectural discussions suggest the following development workflow.

```text
Theory
   ↓
Simulation
   ↓
Servo Testing
   ↓
Single Joint Prototype
   ↓
Single Leg Prototype
   ↓
Inverse Kinematics Implementation
   ↓
Standing Stability
   ↓
Walking Gait Generation
   ↓
Full Quadruped Integration
```

---

# Early Gait Planning Concepts

Initial discussions and sketches indicate exploration of:

- Leg synchronization
- Alternating movement patterns
- Stability during locomotion
- Dynamic balancing
- Weight shifting
- Movement sequencing

These systems will later evolve into:

- Gait generation algorithms
- Stability controllers
- Motion planning systems
- Real-time movement correction

---

# Current Engineering Focus

## Current Priorities

- Understanding inverse kinematics mathematically
- Defining robot architecture
- Planning the first mechanical prototype
- Structuring documentation
- Preparing for servo testing

## Immediate Physical Goal

```text
Achieve stable and mathematically controlled movement of a single robotic leg.
```

---

# Future Expansion

Future versions of the project may include:

- 3 DOF leg architecture
- Computer vision
- Autonomous navigation
- Terrain adaptation
- Sensor fusion
- Real-time balancing
- AI-assisted movement
- Reinforcement learning systems

---

# Conclusion

This document represents the foundational mathematical phase of the quadruped robot project.

The derivations and geometric analysis documented here provide the theoretical framework required for:

- Precise robotic leg movement
- Coordinate-based motion control
- Walking gait development
- Stability analysis
- Future autonomous locomotion systems

The long-term goal of this project is to create a transparent, reproducible, and well-documented open-source robotics platform that helps students, makers, and developers understand how real robotic systems are engineered from the ground up.
