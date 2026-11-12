## About Me

👋 Hi, I'm Varun, a Robotics M.S. student at Northeastern University. Before grad school, I worked as an AI Engineer at DRDO's Research Centre Imarat, training vision-language models and deploying them on Jetson-class robot hardware for real-time perception. I like the part of robotics where models leave the notebook and have to work on a real machine.

🎯 **Open to Spring 2027 co-op roles** in robot perception, SLAM, and robotics software.

## 🧠 Areas of Interest

- Robot perception: detection, segmentation, and vision-language models
- SLAM, sensor fusion, and knowing when a sensor can't be trusted
- Getting models to run fast and reliably on edge hardware (quantization, pruning, distillation)
- Motion planning for manipulators and mobile robots

### 🤖 Selected Robotics Projects

<table>
<tr>

<td width="33%" valign="top">

**Stereo to Mono Vision with ORB-SLAM3**

Detecting the point where a degrading stereo camera becomes no better than mono, before SLAM tracking fails.

[GitHub →](https://github.com/Varun-Ponugoti/Stereo2Mono)

<details>
<summary>Read more</summary>
<br>

A stereo camera that degrades slowly is dangerous because SLAM keeps running without any warning until tracking collapses. We tested whether there's a detectable crossover point where stereo stops beating mono, and trained a health monitor to catch it in real time. [Your role, e.g., "I ran the degradation experiments for blur and occlusion and built the feature extraction pipeline."] Team of 5.

- **Domain:** Visual SLAM · **Dataset:** TUM-VI
- **Tools:** ORB-SLAM3, ResNet18 + GRU health monitor
- **Result:** Distinct failure signatures across 5 degradation types; the health monitor detects the crossover point at 80% accuracy

</details>

</td>
  
<td width="33%" valign="top">

**Mobott: Mobile Robot Platform**

An ESP32 differential-drive robot that localizes itself from an overhead camera, plans with RRT*, and follows people with YOLOv8.

[GitHub →](https://github.com/shyam-sreenivasan/Mobott)

<details>
<summary>Read more</summary>
<br>

A small robot with no wheel encoders or IMU still needs to know where it is to navigate. We gave it global pose feedback from an overhead camera: homography calibration of the table plane plus ArUco markers, which feeds an RRT* planner and a low-level path-tracking controller. I worked across the stack: ESP32 firmware commands in C++, robot behaviors in Python, the ROS 2 interface, camera localization, planning and control, and a MuJoCo model of the robot for RL. Team of 2 (collaborator).

- **Domain:** Mobile robotics · **Hardware:** ESP32 car, iPhone camera, ultrasonic sensor
- **Tools:** ROS 2, OpenCV, ArUco, YOLOv8, RRT*, MuJoCo, Docker
- **Result:** Closed-loop tabletop navigation from camera pose feedback; measured turn rate (8.5 vs assumed 7.0 ms/deg) raised home-return view match from 0.67 to 0.91; fail-safe stop after 300 ms of lost comms

</details>

</td>


<td width="33%" valign="top">

**Dynamic Trajectory Replanning for a 7-DoF Manipulator**

Replanning a robot arm's path in real time when obstacles move.

[GitHub →](https://github.com/Varun-Ponugoti/PANDA-R2P)

<details>
<summary>Read more</summary>
<br>

A plan that was collision-free a second ago can be wrong now if something moves into the arm's path. We reproduced and adapted a dynamic replanning framework in PyBullet, combining RRT-Connect, trajectory optimization, and path rewiring, with custom bounding volumes for faster collision checks. [Your role.] [Team size, or remove if solo.]

- **Domain:** Manipulation · **Simulator:** PyBullet
- **Methods:** RRT-Connect, trajectory optimization, path rewiring, custom bounding volumes
- **Result:** [Add a number, e.g., success rate, replanning time, or collisions avoided]

</details>

</td>

</tr>
</table>

---
