# Cooperative Driver Messaging System (DMS)
### V2X-Based Intent Sharing for Safer and Smarter Driving

---

## Overview

This project introduces a **Cooperative Driver Messaging System (DMS)** that enables vehicles to **communicate driving intent directly to nearby vehicles** using Vehicle-to-Everything (V2X) communication.

Unlike traditional systems that rely only on sensors, DMS allows vehicles to:

- Share **driver intent (e.g., lane change)**
- Improve **situational awareness**
- Reduce ambiguity in driving decisions

---

## Motivation

Most driving conflicts arise from **lack of communication between drivers**.

According to traffic safety studies:
- A large portion of accidents are caused by **driver decision errors**
- Vehicles today cannot directly communicate **intent**

👉 DMS bridges this gap by enabling:

> **explicit, real-time communication between vehicles**

---

## Concept

<p align="center">
  <img src="assets/diagrams/dms_lane_change.png" width="600">
</p>

A host vehicle (HV):
- Detects its own intent (e.g., lane change)
- Identifies a relevant **target vehicle (TV)**
- Sends a **Driver Intent Message (DIM)**

The target vehicle:
- Receives the message
- Gains early awareness of the maneuver
- Can react safely and smoothly

---

## System Architecture

<p align="center">
  <img src="assets/diagrams/dms_architecture.png" width="600">
</p>

The system consists of:

- **Local Object Map**
  - Built using V2X + onboard sensing  
- **Application Detection**
  - Detects driving scenarios (e.g., lane change)  
- **Target Vehicle Selection**
  - Identifies the most relevant vehicle  
- **V2X Communication**
  - Transmits intent messages (DIMs)  

---

## Key Innovation

### 🔹 Intent-Aware Communication

Instead of broadcasting raw data:
- Vehicles send **meaningful, scenario-specific messages**
- Communication becomes **context-aware**

---

### 🔹 Target Vehicle Identification

- Uses **relative position + path history**
- Identifies the vehicle most impacted by the maneuver

From the paper:
- Path-history-based reasoning improves accuracy in curved roads :contentReference[oaicite:3]{index=3}  

---

### 🔹 Cooperative Situational Awareness

DMS extends awareness beyond:
- sensor range
- line-of-sight limitations

Vehicles gain:
- earlier reaction time
- improved safety margins

---

## Example: Lane Change Assistance

- HV intends to change lane  
- System detects scenario  
- Closest vehicle in adjacent lane is identified  
- HV sends intent message  

👉 Result:
- Reduced uncertainty  
- Increased time and space headway  
- Safer maneuver execution  

---

## Applications

- Lane change assistance  
- Intersection negotiation  
- Tailgating warning  
- Cooperative driving in dense traffic  

---

## Key Insights

- Communication of **intent** is more valuable than raw data  
- V2X enables **cooperative decision-making**  
- Early awareness improves safety and comfort  
- System works in both **straight and curved road scenarios** :contentReference[oaicite:4]{index=4}  

---

## Tech Stack

- V2X Communication (DSRC / C-V2X)
- Sensor fusion (radar, CAN bus)
- Embedded vehicle systems
- Algorithmic target selection

---

## Publications & Intellectual Property

- *Enabling a Cooperative Driver Messenger System for Lane Change Assistance* — IEEE ITSC 2022  
- US Patent Application: *Systems and Methods for a Point-to-Point Driver Messenger for Advanced Cooperative Situational Awareness* :contentReference[oaicite:5]{index=5}  
- US Patent: *Systems and Methods for Use in Allocating Parking Spaces* :contentReference[oaicite:6]{index=6}  

---

## Author

Shahriar Shahram  
PhD Candidate — Electrical & Computer Engineering  
University of Central Florida  

---

## Notes

This repository presents a **high-level system view** of the Driver Messaging concept.  
Implementation details are abstracted to respect intellectual property considerations.
