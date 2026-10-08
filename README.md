# V2V-Enabled ADAS Hardware-in-the-Loop Vehicle Simulator

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=165&section=header&text=V2V-ENABLED%20ADAS%20HIL%20VEHICLE%20SIMULATOR&fontSize=27&fontColor=ffffff&animation=fadeIn&fontAlignY=42" alt="V2V-Enabled ADAS HIL Vehicle Simulator"/>

<strong>Hardware-in-the-loop automotive simulation for V2V-enabled ADAS development and testing.</strong>

<br><br>

![MATLAB](https://img.shields.io/badge/MATLAB-orange?logo=mathworks&logoColor=white)
![Simulink](https://img.shields.io/badge/Simulink-Control%20Modeling-orange?logo=mathworks&logoColor=white)
![RoadRunner](https://img.shields.io/badge/RoadRunner-3D%20Simulation-2C3E50)
![ADAS](https://img.shields.io/badge/Domain-ADAS-blue)
![V2V](https://img.shields.io/badge/Communication-V2V-informational)
![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

## 🚗 Overview

A **hardware-in-the-loop vehicle simulator** that connects physical driving controls with **MATLAB/Simulink and RoadRunner** for V2V-enabled ADAS development and scenario-based testing.

The simulator provides a controlled virtual environment for vehicle control, collision avoidance, and Indian-road traffic scenarios without requiring a physically moving autonomous vehicle.

---

## ✨ Key Features

- 🎮 **HIL Driving Interface** — Steering wheel, accelerator, and brake controls connected to the simulation.
- 📡 **V2V Communication** — Vehicle-state exchange for cooperative driving and safety functions.
- 🛡️ **ADAS Functions** — Development platform for safety concepts such as AEB.
- 🌐 **3D Simulation** — RoadRunner-based virtual vehicle and traffic scenarios.
- 🔄 **MATLAB Integration** — MATLAB/Simulink control and simulation workflow.
- 🧪 **Scenario Testing** — Repeatable multi-vehicle scenarios for testing and validation.

---

## 🎥 Project Demonstration

### 🕹️ Hardware-in-the-Loop Setup

<p align="center">
  <img src="./assets/Hardware_setup.png" width="850" alt="Hardware-in-the-Loop setup"/>
</p>

### 🛣️ RoadRunner Highway Scenario

<p align="center">
  <img src="./assets/Highway_merge_control.jpeg" width="850" alt="RoadRunner highway merge control scenario"/>
</p>

---

## 🧩 System Architecture

```mermaid
flowchart LR

    H["🎮 Steering Wheel<br/>Accelerator + Brake"]

    M["MATLAB / Simulink"]

    RR["RoadRunner<br/>3D Vehicle Simulation"]

    V2V["📡 V2V<br/>Vehicle Data"]

    ADAS["🛡️ ADAS<br/>Safety Logic"]

    R["📊 Results &<br/>Scenario Analysis"]

    H --> M
    M <--> RR

    RR --> V2V
    V2V --> ADAS

    M --> ADAS
    ADAS --> M

    M --> R
    RR --> R
