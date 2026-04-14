# Cooperative Driver Messaging System (DMS)
### V2X-Based Intent Sharing for Safer and Smarter Driving

---

## Overview

This project introduces a **Cooperative Driver Messaging System (DMS)** that enables vehicles to **communicate driving intent directly to nearby vehicles** using Vehicle-to-Everything (V2X) communication.

Unlike traditional systems that rely only on sensors, DMS allows vehicles to:

- Share **driver intent (e.g., lane change)**
- Improve **situational awareness**
- Reduce ambiguity in driving decisions
- Enable **cooperative driving behavior**

---

## Motivation

Many driving conflicts arise due to **lack of explicit communication between drivers**.

Traditional systems:
- Infer intent from motion (often too late)
- Cannot communicate planned maneuvers
- Lead to uncertainty and delayed reactions

👉 DMS addresses this by enabling:

> **Direct, real-time communication of driver intent between vehicles**

---

## Concept: Intent Sharing in Driving

<p align="center">
  <img src="assets/diagrams/dms_lane_change.png" width="600">
</p>

A host vehicle (HV):
- Detects its driving intent (e.g., lane change)
- Identifies a relevant **target vehicle (TV)**
- Sends a **Driver Intent Message (DIM)**

The target vehicle:
- Receives the message
- Gains early awareness of the maneuver
- Responds safely and smoothly

---

## Target Vehicle Identification

<p align="center">
  <img src="assets/diagrams/dms_target_selection.png" width="600">
</p>

Key idea:
- Identify the **most relevant vehicle** affected by the maneuver

The system uses:
- Relative position
- Lane difference (lateral distance)
- Path history information

✔ Works in both straight and curved road scenarios  

---

## System Architecture

The system consists of:

- **Local Object Map**
  - Built using V2X + onboard sensing  

- **Application Detection**
  - Detects driving scenarios (e.g., lane change)  

- **Target Vehicle Selection**
  - Identifies the vehicle most affected  

- **V2X Communication**
  - Transmits Driver Intent Messages (DIMs)  

---

## Simulation Environment

<p align="center">
  <img src="assets/diagrams/dms_simulation.png" width="600">
</p>

- Evaluated using **SUMO + CARLA**
- Multi-vehicle traffic scenarios
- Realistic urban environments
- Enables validation of cooperative behavior under traffic interactions

---

## Key Insights

- Communication of **intent** is more valuable than raw sensor data  
- Early awareness improves **safety and comfort**  
- V2X enables **cooperative decision-making**  
- Reduces uncertainty in multi-vehicle interactions  
- Improves lane-change safety and traffic flow  

---

## Applications

- Lane change assistance  
- Intersection coordination  
- Tailgating mitigation  
- Cooperative autonomous driving  

---

## Publications & Intellectual Property

- *Enabling a Cooperative Driver Messenger System for Lane Change Assistance* — IEEE ITSC 2022  
- US Patent Application: *Point-to-Point Driver Messenger for Cooperative Situational Awareness*  
- Related work in cooperative vehicle systems  

---

## Author

Shahriar Shahram  
PhD Candidate — Electrical & Computer Engineering  
University of Central Florida  

---

## Notes

This repository presents a **high-level system overview** of the Driver Messaging concept.  
Implementation details are abstracted to respect intellectual property considerations.
