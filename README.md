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

A stereo camera that degrades slowly is dangerous because SLAM keeps running without any warning until tracking collapses. We tested whether there's a detectable crossover point where stereo stops beating mono, and trained a health monitor to catch it in real time. I designed and trained the ResNet-18 + GRU health monitor that predicts, from image sequences alone, when the stereo setup has degraded past the switch point. Team of 5.

- **Domain:** Visual SLAM · **Dataset:** TUM-VI
- **Tools:** ORB-SLAM3, ResNet18 + GRU health monitor
- **Result:** Distinct failure signatures across 5 degradation types; the health monitor detects the crossover point at 80% accuracy

</details>

</td>

<td width="33%" valign="top">

**Mobott: Mobile Robot Platform**

A ROS 2 mobile robot that localizes itself from an overhead camera, plans with RRT*, and follows the path on real hardware.

[GitHub →](https://github.com/shyam-sreenivasan/Mobott)

<details>
<summary>Read more</summary>
<br>

A small differential-drive robot runs its motors open-loop, so it can't measure where it actually went. We gave it eyes from outside: an overhead camera localizes it from an ArUco marker, an RRT* planner plans a path to the goal, and a low-level controller follows that path using the camera's pose feedback. I worked across the stack, including the RRT* planning, path-following control, homography-based camera calibration, ESP32 firmware in C++, and the ROS 2 interfaces. We also modeled the robot in MuJoCo for RL experiments. Team of 2.

- **Domain:** Mobile robotics · **Hardware:** ESP32 differential-drive robot, iPhone camera
- **Tools:** ROS 2, OpenCV (ArUco, homography), RRT*, YOLOv8, MuJoCo, Docker
- **Result:** Closed-loop goal navigation on real hardware; measuring the true turn rate (8.5 vs. an assumed 7.0 ms/deg) raised home-return view match from 0.67 to 0.91; fail-safe stop after 300 ms of lost comms

</details>

</td>

<td width="33%" valign="top">

**Dynamic Trajectory Replanning for a 7-DoF Manipulator**

Replanning a robot arm's path in real time when obstacles move.

[GitHub →](https://github.com/Varun-Ponugoti/PANDA-R2P)

<details>
<summary>Read more</summary>
<br>

A plan that was collision-free a second ago can be wrong now if something moves into the arm's path. We reproduced and adapted a dynamic replanning framework in PyBullet, combining RRT-Connect, trajectory optimization, and path rewiring, with custom bounding volumes for faster collision checks. I implemented RRT-Connect, the collision checker, and trajectory generation, and drove the arm with PID control through ROS 2. Team of 2.

- **Domain:** Manipulation · **Simulator:** PyBullet
- **Methods:** RRT-Connect, trajectory optimization, path rewiring, custom bounding volumes
- **Result:** 100% success across 30 trials, rerouting around obstacles in under 0.5 s, with planned paths simplified by over 80%

</details>

</td>

</tr>
</table>

---
