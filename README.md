# PROJECT — Cartesian Laser Engraver / Cutter
<img width="4000" height="2252" alt="20260528_104314" src="https://github.com/user-attachments/assets/e595b193-009e-4e07-8137-7ab41329e488" />

## Overview
Custom-built laser engraver/cutter developed from the **PROJECT-Cartesian-Origins** platform. The system re-engineers a Cartesian motion base into a modular, high-precision fabrication machine capable of laser engraving and light-to-medium duty cutting.

Designed for both personal prototyping and scalable commercial workflows, the platform emphasizes modularity, firmware flexibility, and real-time control integration.

**Project Status:** Actively in development (as of May 28, 2026)

---

## System Concept
This machine repurposes a Cartesian motion system (X/Y/Z architecture) into a digitally controlled fabrication tool. The design prioritizes:

- Precision motion control across all axes
- Modular hardware expansion
- Firmware-level adaptability
- Clean conversion from CAD → machine execution

---

## Software Stack

### Motion Control Firmware
- **FluidNC** — An open-source motion control firmware running on ESP32-based systems. It handles real-time G-code execution, stepper motor control, and hardware interfacing for CNC and laser systems.  
  :contentReference[oaicite:0]{index=0}  
  https://github.com/bdring/FluidNC

### Design & Control Interface
- **LaserGRBL** — A lightweight G-code sender and laser control application used to convert images and vector designs into machine-executable motion paths. It supports engraving workflows, power modulation, and real-time job control.  
  :contentReference[oaicite:1]{index=1}  
  https://lasergrbl.com

### Embedded Hardware
- **ESP32** microcontroller platform used as the primary control unit for motion processing and real-time command execution.  
  ESP32

---
<img width="4000" height="2252" alt="20260528_102955" src="https://github.com/user-attachments/assets/2146c4f7-469f-494b-91be-17d3a73f37ed" />

## System Workflow

1. **Design Input**
   - Images, vectors, or CAD outputs are processed in LaserGRBL

2. **G-code Generation**
   - LaserGRBL converts designs into optimized motion paths and laser power profiles

3. **Communication Layer**
   - G-code is transmitted to the controller via serial/Wi-Fi interface

4. **Embedded Execution**
   - FluidNC running on ESP32 interprets G-code in real time

5. **Mechanical Output**
   - Cartesian motion system executes precise engraving/cutting operations

---

## Key Features

- Cartesian-based motion system (X/Y/Z expandable)
- Laser engraving and cutting capability
- ESP32-based wireless/serial control
- Real-time G-code execution via FluidNC
- Modular architecture for future toolhead upgrades
- CAD-to-machine workflow integration

---

## Engineering Focus

This project integrates multiple disciplines:

- Embedded systems programming (ESP32 firmware integration)
- Motion control systems (stepper-driven Cartesian kinematics)
- Computer-aided manufacturing (G-code pipeline)
- Electrical and mechanical system integration
- Laser safety and power modulation control

---

## Future Work

- Closed-loop feedback system integration
- Camera-assisted alignment / computer vision positioning
- Automated calibration routines
- Multi-material cutting profiles
- Web-based control dashboard for remote operation
