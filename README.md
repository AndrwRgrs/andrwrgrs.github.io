# Robotics Engineer
I am a Mechatronics Engineer (MASc) specializing in the intersection of physical systems and safety-critical firmware. Currently, I lead the controls and system architecture for production-scale robotics at GlüxKind. I thrive on 'Creative Destruction'—identifying architectural bottlenecks and replacing them with scalable, high-performance C++ solutions. From designing impedance control laws to architecting AWS-managed OTA engines, I build the brains that make hardware move intelligently.
### Education
- MASc Mechanical Engineering | University of Toronto | June 2021 - August 2023
    - Thesis: Occupancy Grid Mapping via Resource-Constrained Robotic Swarms: A Collaborative Exploration Strategy
    - Supervisors: Prof. Beno Benhabib & Prof. Goldie Nejat

- BASc Mechanical Engineering | University of Toronto | September 2016 - May 2021
    - Specialization: Mechatronics and Solid Mechanics
    - CGPA: 3.74/ 4.0

### Work Experience
**Graduate Research Assistant | University of Toronto | May 2021 - August 2023**
- Succesfully developed a novel exploration and mapping strategy for robotic swarms of 40+ mobile robots, leveraging stochastic area coverage motion strategies and fast, efficient frontier-based exploration strategies to explore quickly while allowing the strategy to remain scalable to a large number of robots.
- Improved the overall environment sensing capabilities of a swarm through effective motion planning and demonstrated these results within a custom-built a swarm robotics simulation environment in Python, resulting in the successful [publication](https://www.mdpi.com/2218-6581/12/3/70) of the work in MDPI Robotics journal.
- Built millimeter-scale robots (mROBerTO) and programmed them in embedded C to perform physical validation experiments of novel swarm algorithms.

**Research and Technology Engineering Intern | Safran Landing Systems Toronto | August 2019- August 2020**
- Led the development and design of a novel additively manufactured component for the piston assembly of an aircraft landing gear; including writing technical documentation and schematics to send to manufacturers.
- Significantly improved and optimized the assembly inspection times for the Boeing 747 nose landing gear by implementing a prototype computer vision-based inspection system. 
- Oversaw the manufacturing of custom-ordered 3D printed parts as the head of the plastic additive manufacturing lab for the R&T department. Implemented experimental hardware and software increasing each printer’s life and providing additional features such as multi-filament prints and a heated print bed with custom GUI interface.


### Projects

#### Multi-Robot Motion Planning Comparison
Conducted a comprehensive assessment of dynamic motion planning algorithms, including implementing from scratch both dynamic sampling-based planners (DRRT*, RRTX) and reactive strategies (velocity obstacles) in Python. The effectiveness of these planners were validated  in a novel multi-robot use case wherein robots could not coordinate with each other and must constantly repair and replan their planned paths to ensure collision-free trajectories.
[Link to project repository](https://github.com/AndrewRgrs/Dynamic-Planners-but-Multi-Robot)

![4 Robots navigating using DRRT*](assests/img/DRRT_Star.gif)


#### State Estimation/Localization of a Stereo Camera in 3D using batch Gauss-Newton Optimization method
The goal of this project was to estimate the state (x,y,z,theta) of a vehicle equipped with a stereo camera and inertial measurement unit (IMU) traveling through a field of landmarks. The entire project was completed in MATLAB from a dataset of noisy measurements from the vehicle. 

The batch Gauss-Newton method was implemented to fuse measurements from the IMU with point measurments from the stereo camera. Since the vehicle could freely translate and rotate through the three-dimensional space, the sets of transformation and rotation matricies used to represent the vehicles position over time were matrix Lie groups SE(3) and SO(3). 
[Link to project repository](https://github.com/AndrewRgrs/stereo_camera_state_estimatation)

![Estimated and Ground Truth Path](assests\img\Path.png)


### Publications
1. **A. Rogers**, K. Eshaghi, G. Nejat, and B. Benhabib, “Occupancy Grid Mapping via Resource-Constrained Robotic Swarms: A Collaborative Exploration Strategy,” MDPI Robotics, vol. 12, no. 3, Art. no. 3, Jun. 2023, [doi: 10.3390/robotics12030070](https://doi.org/10.3390/robotics12030070).
2. K. Eshaghi, **A. Rogers**, G. Nejat, and B. Benhabib, “Closed-Loop Motion Control of Robotic Swarms – A Tether-Based Strategy,” IEEE Transactions on Robotics, vol. 38, no. 6, pp. 3564–3581, Dec. 2022, [doi: 10.1109/TRO.2022.3181055](https://doi.org/10.1109/TRO.2022.3181055). 


#### Technical Skills: 
- **Programming** : Python, MATLAB, C++, Arduino   
- **CAD** : SolidWorks, Catia V5, Fusion 360   
- **Robotics** : Sensor Fusion, Motion Planning, ROS Experience
- **Additive Manufacturing** : FDM, SLA, DFAM


