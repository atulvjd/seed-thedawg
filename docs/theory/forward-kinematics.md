# Forward Kinematics

## Overview

Forward kinematics is the process of calculating the endpoint position of the robotic leg using known joint angles and link lengths.

Unlike inverse kinematics:
- Forward kinematics calculates position from angles
- Inverse kinematics calculates angles from position

---

# System Variables

| Variable | Description |
|---|---|
| l1 | Upper leg length |
| l2 | Lower leg length |
| θ1 | Hip angle |
| θ2 | Knee angle |

---

# Endpoint Position Equations

## X Coordinate

```text
x = l1cos(θ1) + l2cos(θ1 + θ2)
```

---

## Y Coordinate

```text
y = l1sin(θ1) + l2sin(θ1 + θ2)
```

---

# Purpose

Forward kinematics is useful for:
- Simulation
- Visualization
- Movement verification
- Testing inverse kinematics accuracy
- Debugging robotic motion

---

# Current Focus

The project currently prioritizes:
- Inverse kinematics implementation
- Coordinate-based movement
- Single leg movement testing