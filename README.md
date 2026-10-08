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
```

## 🛠️ Tech Stack

### Hardware
![Steering Wheel](https://img.shields.io/badge/Steering%20Wheel-HIL%20Controller-555555)
![Accelerator](https://img.shields.io/badge/Accelerator-Pedal-555555)
![Brake](https://img.shields.io/badge/Brake-Pedal-555555)

### Software & Tools
![MATLAB](https://img.shields.io/badge/MATLAB-Modeling-orange?logo=mathworks&logoColor=white)
![Simulink](https://img.shields.io/badge/Simulink-Control%20Modeling-orange?logo=mathworks&logoColor=white)
![RoadRunner](https://img.shields.io/badge/RoadRunner-3D%20Simulation-2C3E50)
![RoadRunner API](https://img.shields.io/badge/RoadRunner%20API-Programmatic%20Control-2C3E50)

### Automotive Concepts
![ADAS](https://img.shields.io/badge/ADAS-Safety%20Systems-blue)
![V2V](https://img.shields.io/badge/V2V-Vehicle%20Communication-informational)
![AEB](https://img.shields.io/badge/AEB-Emergency%20Braking-critical)

## 📊 Results & Highlights

| Area | Current Status |
|---|---|
| HIL driving interface | In development |
| RoadRunner 3D simulation | In development |
| MATLAB–RoadRunner control | In development |
| V2V functionality | In development |
| ADAS functions | In development |
| Quantitative benchmark | <!-- ADD: measured latency / accuracy / test count --> |

> Quantitative performance values will be added after measurement and validation.

## ✅ Requirements

- [ ] MATLAB
- [ ] Simulink
- [ ] RoadRunner
- [ ] RoadRunner Scenario
- [ ] Compatible steering-wheel + pedal controller
- [ ] Required MATLAB/Simulink interfaces for the implemented modules
- [ ] <!-- ADD: exact MATLAB/RoadRunner release -->
- [ ] <!-- ADD: additional toolbox/package dependencies -->

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Abhishek3m4/V2V-Enabled-ADAS-Hardware-in-the-Loop-Vehicle-Simulator.git
cd V2V-Enabled-ADAS-Hardware-in-the-Loop-Vehicle-Simulator
```

### 2. Configure the simulation environment

Open the project in MATLAB and configure your local RoadRunner installation and project paths.

```matlab
% Example only — replace with your local paths.
rrInstallationPath = "C:\Path\To\RoadRunner\bin\win64";
rrProjectPath      = "C:\Path\To\RoadRunnerProject";
```

### 3. Connect the HIL controller

Connect the steering wheel, accelerator and brake pedals to the PC and verify that the controller is detected by the operating system.

### 4. Run the simulation

Open the relevant MATLAB/Simulink model or MATLAB control script from the repository and launch the RoadRunner scenario.

```matlab
% ADD: exact project launch script / Simulink model name
```

> **Repository status:** The public repository is currently being built out; exact runnable file names and dependency versions will be added as implementation is committed.

## 📁 Project Structure

```text
V2V-Enabled-ADAS-Hardware-in-the-Loop-Vehicle-Simulator/
├── README.md              # Project overview, workflow and setup
├── LICENSE                # MIT license
├── matlab/                # <!-- ADD: MATLAB scripts/functions -->
├── simulink/              # <!-- ADD: Simulink models -->
├── roadrunner/            # <!-- ADD: RoadRunner scenes/scenarios -->
├── hardware/              # <!-- ADD: HIL/controller integration -->
├── v2v/                   # <!-- ADD: V2V communication modules -->
├── adas/                  # <!-- ADD: ADAS logic / algorithms -->
├── results/               # <!-- ADD: logs, plots and validation results -->
└── assets/                # <!-- ADD: README screenshots/GIFs -->
```

## 🏆 Achievements / Publications

<!-- ADD only when directly applicable to this repository:
- Hackathon / competition achievement
- Award
- Publication / DOI
-->

## 👨‍💻 Author

<div align="center">

### Abhishek Ahirrao
**B.Tech E&TC | Embedded Systems • Automotive • VLSI**

<a href="https://github.com/Abhishek3m4">
  <img src="https://img.shields.io/badge/GitHub-Abhishek3m4-181717?logo=github&logoColor=white" alt="GitHub"/>
</a>
<!-- ADD: LinkedIn URL -->
<!-- ADD: Portfolio URL -->
<a href="mailto:abhishekahirrao3m4@gmail.com">
  <img src="https://img.shields.io/badge/Email-Contact-D14836?logo=gmail&logoColor=white" alt="Email"/>
</a>

</div>

## 📄 License

This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

<div align="center">

**Built for automotive simulation, ADAS development and hardware-in-the-loop testing.**

</div>
