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
<td width="50%" valign="top">

**Single and Multi-Object Recognition**

One detector that names a single object or finds every object in a crowded image: 94.2% classification accuracy, 0.806 mAP50 detection.

[GitHub →](https://github.com/Varun-Ponugoti/DLAI)

<details>
<summary>Read more</summary>
<br>

The dataset only had photos of one object at a time, but the system also had to find many objects in one image. So we built the multi-object data ourselves: pasting single photos into grids, transforming their box labels, and splitting train/val/test *before* compositing so no test photo leaks into training. Boxes were auto-labeled with Grounding DINO instead of drawn by hand. [Your role, e.g., "I built the grid dataset pipeline and trained and evaluated the YOLOv8 detector."] Team of 4.

- **Domain:** Object recognition · **Dataset:** 7,315 custom photos, 73 classes
- **Models:** Baseline CNN, MobileNetV2, ResNet50, EfficientNetB0, YOLOv8s
- **Result:** EfficientNetB0 at 94.2% test accuracy (5.7× smaller than ResNet50 at similar accuracy); YOLOv8s at 0.806 mAP50 / 0.765 mAP50-95 on 561 test grids, 12 ms per image

</details>

</td>
<td width="50%" valign="top">

**Stereo Camera Health Monitor for ORB-SLAM3**

Detecting the point where a degrading stereo camera becomes no better than mono, before SLAM tracking fails.

[GitHub →](https://github.com/shyam-sreenivasan/Stereo-Camera-Health-Monitor-For-ORB-SLAM3)

<details>
<summary>Read more</summary>
<br>

A stereo camera that degrades slowly is dangerous because SLAM keeps running without any warning until tracking collapses. We tested whether there's a detectable crossover point where stereo stops beating mono, and trained a health monitor to catch it in real time. [Your role, e.g., "I ran the degradation experiments for blur and occlusion and built the feature extraction pipeline."] Team of 5.

- **Domain:** Visual SLAM · **Dataset:** TUM-VI
- **Tools:** ORB-SLAM3, ResNet18 + GRU health monitor
- **Result:** Distinct failure signatures across 5 degradation types; the health monitor detects the crossover point at 80% accuracy

</details>

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Dynamic Trajectory Replanning for a 7-DoF Manipulator**

Replanning a robot arm's path in real time when obstacles move.

[GitHub →](https://github.com/Varun-Ponugoti/REPO)

<details>
<summary>Read more</summary>
<br>

A plan that was collision-free a second ago can be wrong now if something moves into the arm's path. We reproduced and adapted a dynamic replanning framework in PyBullet, combining RRT-Connect, trajectory optimization, and path rewiring, with custom bounding volumes for faster collision checks. [Your role.] [Team size, or remove if solo.]

- **Domain:** Manipulation · **Simulator:** PyBullet
- **Methods:** RRT-Connect, trajectory optimization, path rewiring, custom bounding volumes
- **Result:** [Add a number, e.g., success rate, replanning time, or collisions avoided]

</details>

</td>
<td width="50%" valign="top">

**Autonomous Mobile Robot for Obstacle Avoidance**

A wheeled robot built from hardware to software that maps, navigates, and avoids obstacles.

[GitHub →](https://github.com/Varun-Ponugoti/REPO)

<details>
<summary>Read more</summary>
<br>

Simulation hides the problems that show up on real hardware: noisy sensors, wheel slip, and timing. This robot uses vision-based perception for obstacle detection and localization, a SLAM pipeline for goal-directed navigation with continuous map updates, and PID control with reactive obstacle avoidance. [Your role.] [Team size, or remove if solo.]

- **Domain:** Mobile robotics · **Platform:** [e.g., Raspberry Pi / Jetson, camera, LiDAR]
- **Methods:** Vision-based detection, SLAM, PID control, real-time replanning
- **Result:** [Add a number, e.g., navigation success rate or goal-reaching accuracy]

</details>

</td>
</tr>
</table>

---
