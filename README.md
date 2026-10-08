# V2V-Enabled ADAS Hardware-in-the-Loop Vehicle Simulator

<div align="center">

<a href="https://github.com/Abhishek3m4/V2V-Enabled-ADAS-Hardware-in-the-Loop-Vehicle-Simulator">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=190&section=header&text=V2V-Enabled%20ADAS%20Hardware-in-the-Loop%20Vehicle%20Simulator&fontSize=34&fontColor=ffffff&animation=fadeIn&fontAlignY=38" alt="Project Header"/>
</a>

<p><strong>Hardware-in-the-loop automotive simulation for V2V-enabled ADAS development and testing.</strong></p>

![MATLAB](https://img.shields.io/badge/MATLAB-orange?logo=mathworks&logoColor=white)
![Simulink](https://img.shields.io/badge/Simulink-Control%20Modeling-orange?logo=mathworks&logoColor=white)
![RoadRunner](https://img.shields.io/badge/RoadRunner-3D%20Simulation-2C3E50)
![ADAS](https://img.shields.io/badge/Domain-ADAS-blue)
![V2V](https://img.shields.io/badge/Communication-V2V-informational)
![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

## 🚗 Overview

A hardware-in-the-loop vehicle simulator that connects **physical driving controls** with **MATLAB/Simulink + RoadRunner** to develop and test V2V-enabled ADAS functions in a controlled virtual environment.

The project focuses on automotive control, scenario-based testing, collision avoidance and Indian-road simulation workflows without requiring a physically moving autonomous vehicle.

## ✨ Key Features

- 🎮 **Hardware-in-the-Loop** — Interface a steering wheel, accelerator and brake pedals with the simulation environment.
- 📡 **V2V Communication** — Exchange vehicle-state information for cooperative driving and safety logic.
- 🛡️ **ADAS Concepts** — Platform for functions such as AEB and vehicle safety assistance.
- 🌐 **3D Vehicle Simulation** — Build and test traffic scenarios in RoadRunner.
- 🔄 **MATLAB Integration** — Control and analyze RoadRunner simulations programmatically from MATLAB.
- 🧪 **Scenario-Based Testing** — Reproduce repeatable multi-vehicle situations for development and validation.

## 🎥 Demo / Screenshots

<div align="center">

| RoadRunner Simulation | HIL Control Setup |
|---|---|
| <!-- ADD: project RoadRunner screenshot --> | <!-- ADD: steering wheel + pedal hardware photo --> |
| *3D traffic / ego-vehicle scenario* | *Physical HIL control interface* |

| ADAS / V2V Test | MATLAB / Simulink |
|---|---|
| <!-- ADD: ADAS event screenshot/GIF --> | <!-- ADD: MATLAB/Simulink model screenshot --> |
| *Collision / safety scenario* | *Control and data-flow model* |

<!-- ADD: Demo GIF or project video link -->

</div>

## 🧩 System Architecture / Workflow

```mermaid
flowchart LR
    H["🎮 HIL Driving Controls<br/>Steering + Accelerator + Brake"]
    PC["💻 Simulation Workstation"]
    M["MATLAB / Simulink"]
    RR["RoadRunner<br/>3D Scene + Scenario"]
    V2V["📡 V2V Data Exchange"]
    ADAS["🛡️ ADAS / Safety Logic"]
    LOG["📊 Simulation Data<br/>Analysis & Validation"]

    H --> PC
    PC --> M
    M <--> RR
    RR --> V2V
    V2V --> ADAS
    M --> ADAS
    ADAS --> M
    M --> LOG
    RR --> LOG
