# Andrew M. Rogers
### **C++ Software Engineer | Systems & Robotics Architect (MASc)**
**Specializing in the intersection of high-performance C++, computer vision, and distributed cloud infrastructure.**

[LinkedIn](https://www.linkedin.com/in/andrew~rogers/) | [Email](mailto:andrew.rogers482@gmail.com)

---

## Professional Summary
I am a Mechatronics Engineer (MASc) operating at the intersection of physical hardware and high-performance software—where raw sensor data becomes actionable insight. I write **production-level modern C++ (14/17/20)** and **Python** for the full stack, from embedded firmware up to AWS-managed cloud services.

Currently, at **GlüxKind**, I serve as Lead Systems Architect, guiding technical decisions, identifying architectural gaps, managing technical debt, and mentoring other developers. My production work spans multi-modal sensor fusion for safety-critical control, high-fidelity simulation in **Nvidia Isaac Sim**, and a fleet OTA engine on **AWS IoT**. My graduate research and projects extend this skill set into **computer vision and 3D perception**—including OpenCV-based swarm robotics and stereo-vision state estimation on matrix Lie groups (SE(3)/SO(3)).

I thrive in the space where the "metal" meets the "math", building the software that lets systems see, understand, and act on the physical world.

---

## Education

**Master of Applied Science (MASc), Mechanical Engineering**
*University of Toronto | 2021 – 2023*
* **Thesis:** Occupancy Grid Mapping via Resource-Constrained Robotic Swarms: A Collaborative Exploration Strategy
* **Supervisors:** Prof. Beno Benhabib & Prof. Goldie Nejat

**Bachelor of Applied Science (BASc), Mechanical Engineering**
*University of Toronto | 2016 – 2021*
* **Specialization:** Mechatronics and Solid Mechanics
* **Academic Standing:** CGPA 3.74/4.0

---

## Featured Experience: GlüxKind Robotics
**Software Engineer: Robotics II (Lead Systems Architect)** | *Jan 2024 – Present*

*Lead the transition from prototype-stage systems to a production-ready, distributed robotics architecture. (Promoted from Robotics I in August 2024).*

Real-Time Systems & Sensor Fusion:
* **Active Safety & Control Systems:** Feature owner for the "User-Intent" detection system. Engineered a multi-modal fusion algorithm (Force Sensors, Ultrasonic Distance, IMU, and Motor Odometry) to drive **Runaway Brake Assist** auto-activation, ensuring 100% reliable detection across all terrain and load conditions.
* **Safety-Critical Controls:** Designed and implemented **Impedance Control** laws for the "Rosa" platform. Solved key challenges in **varying payload tuning**, prioritizing safe, predictable, and deterministic vehicle behavior. Developed custom braking profiles to minimize wheel slip while maintaining smooth deceleration.
* **State Estimation & Sensor Fusion:** Engineered a robust state estimation pipeline using an **Extended Kalman Filter (EKF)** to fuse high-frequency IMU and encoder data for precise attitude determination in unstructured environments.
* **Ultrasonic DSP & IMM Kalman Filter:** Implemented a custom **Interacting Multiple Model (IMM) Kalman filter** — adapted from published literature, written without external controls libraries — to extract user distance and relative velocity from noisy, pre-filtered ultrasonic returns. Optimized for deterministic real-time execution on embedded hardware.
* **Autonomy Simulation & Validation:** Spearheaded the migration from ROS1 to **ROS2** and developed high-fidelity validation environments in **Nvidia Isaac Sim**. Leveraged simulation to verify corner-case safety behaviors (e.g., autonomous doorway entry) before physical deployment.
* **Real-Time Audio Pipeline Overhaul:** Re-architected a multi-threaded embedded audio pipeline to eliminate jitter and dropouts caused by concurrent SD-card I/O. Decoupled the audio sink from storage access via asynchronous buffering and a custom mutex-protected SD-card driver wrapper, taking the system from frequent multi-second delays and audio artifacts to imperceptible playback under sustained load.

Cloud, Data & Developer Tooling:
* **Protobuf Telemetry Pipeline:** Architected a new telemetry pipeline using **Google Protocol Buffers (Proto3)**, replacing legacy CSV logging. Achieved a **10x throughput increase**, enabling synchronized capture of high-frequency sensor data and asynchronous system logs for root-cause analysis.
* **Python Telemetry Visualization Suite:** Designed and authored ~90% of an internal **Dash/Plotly** web application (Pandas/NumPy/SciPy) that decodes the Protobuf telemetry stream — including COBS/CRC framing — and renders interactive time-series charts, geospatial maps (Folium), and multi-signal overlays. Relied on daily by the firmware team for log triage and root-cause analysis.
* **Production OTA & Fleet Management:** Engineered a robust Over-the-Air (OTA) engine using **AWS IoT Jobs over MQTT**. Implemented a custom state machine with **A/B partition switching** and RAM-buffered downloads to ensure zero-brick reliability, reducing nominal update cycles by 83% (from 30m to 5m).
* **Field Observability:** Authored a lightweight **"Error Relay" middleware** utilizing asynchronous BLE payloads and NVS persistence to ensure critical fault visibility even in low-connectivity (non-WiFi) environments.
* **Architecture & Code-Quality Practice:** Author RFCs and feature-architecture proposals to align the team on technical direction; enforce **Doxygen-level documentation** on all PRs to keep the codebase navigable as the team scales.


![ROSA Stroller](assests/img/CruiseControlPAS.gif) ![Brake Assist](assests/img/BrakeAssist.gif)

---

## Research Focus: Swarm Robotics & Mapping
**Graduate Research Assistant | University of Toronto | 2021 – 2023**

Developed strategies for **resource-constrained collaborative mapping** in large-scale swarms (40+ units), focusing on stochastic area coverage and frontier-based exploration.

* **Hardware-in-the-Loop:** Programmed millimeter-scale robots (**mROBerTO**) in **Embedded C** to physically validate swarm algorithms.
* **Research Publication & Simulation:** Developed a novel exploration and mapping strategy for large-scale swarms using stochastic motion and frontier-based techniques, validated through a custom-built Python simulation environment and [published](https://www.mdpi.com/2218-6581/12/3/70) in the **MDPI Robotics** journal.



---

## Technical Projects

### **High-Dimensional State Estimation**
The goal of this project was to estimate the 3D state (position and orientation) of a vehicle from a noisy stereo camera and inertial measurement unit (IMU) traveling through a field of landmarks. 

The batch Gauss-Newton method was implemented to fuse measurements from the IMU with point measurements from the stereo camera. Since the vehicle could freely translate and rotate through three-dimensional space, the sets of transformation and rotation matrices used to represent the vehicle's position over time were matrix Lie groups **SE(3)** and **SO(3)**.

[View Project Repository](https://github.com/AndrwRgrs/stereo_camera_state_estimatation)

![Estimated and Ground Truth Path](assests/img/Path.png)

### **Dynamic Motion Planning Comparison**
This project involved the implementation and comparison of various motion planning algorithms for real-time path repair in uncoordinated multi-robot environments. Algorithms including **DRRT***, **RRTX**, and **Velocity Obstacles** were developed from scratch in Python to assess their efficiency in dynamic obstacle avoidance. The effectiveness of these planners were validated in a novel multi-robot use case wherein robots could not coordinate with each other and must constantly repair and replan their planned paths to ensure collision-free trajectories.

[View Project Repository](https://github.com/AndrwRgrs/Dynamic-Planners-but-Multi-Robot)

![4 Robots navigating using DRRT*](assests/img/DRRT_Star.gif)

---

## Technical Toolkit

| Domain | Skills |
| :--- | :--- |
| **Languages** | C++ (14/17/20), Python, MATLAB, Embedded C |
| **Firmware/IoT** | ESP-IDF, FreeRTOS, AWS IoT, MQTT, Protobuf, BLE, I2C/UART/SPI |
| **Robotics/Controls** | ROS2, Sensor Fusion (EKF, IMM Kalman), Impedance Control, Matrix Lie Groups |
| **Vision/Graphics** | OpenCV, Stereo Vision, State Estimation (SE(3)/SO(3)) |
| **Data/Visualization** | Dash, Plotly, Pandas, NumPy, SciPy, Folium |
| **Simulation** | Nvidia Isaac Sim, Gazebo, Custom Python Environments |
| **Mechanical** | Solid Mechanics, SolidWorks, CATIA V5, Altium Designer, DFAM |

---

## Publications
1. **A. Rogers**, K. Eshaghi, G. Nejat, and B. Benhabib, “Occupancy Grid Mapping via Resource-Constrained Robotic Swarms: A Collaborative Exploration Strategy,” MDPI Robotics, vol. 12, no. 3, Art. no. 3, Jun. 2023, [doi: 10.3390/robotics12030070](https://doi.org/10.3390/robotics12030070).
2. K. Eshaghi, **A. Rogers**, G. Nejat, and B. Benhabib, “Closed-Loop Motion Control of Robotic Swarms – A Tether-Based Strategy,” IEEE Transactions on Robotics, vol. 38, no. 6, pp. 3564–3581, Dec. 2022, [doi: 10.1109/TRO.2022.3181055](https://doi.org/10.1109/TRO.2022.3181055). 

---

### **Let's Connect**
I’m driven by projects that require a deep understanding of both the "metal" and the "math." 

[LinkedIn](https://www.linkedin.com/in/andrew~rogers/) | [Email](mailto:andrew.rogers482@gmail.com) | [GitHub](https://github.com/AndrwRgrs) 

