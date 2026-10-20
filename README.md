## About Me

👋 Hi, I'm Varun, a Robotics M.S. student at Northeastern University. Before grad school, I worked as an AI Engineer at DRDO's Research Centre Imarat, training vision-language models and deploying them on Jetson-class robot hardware for real-time perception. I like the part of robotics where models leave the notebook and have to work on a real machine.

🎯 **Open to Spring 2027 co-op roles** in robot perception, SLAM, and robotics software.

## 🧠 Areas of Interest

- Robot perception: detection, segmentation, and vision-language models
- SLAM, sensor fusion, and knowing when a sensor can't be trusted
- Getting models to run fast and reliably on edge hardware (quantization, pruning, distillation)
- Motion planning for manipulators and mobile robots

## 🚧 Currently Working On

**[Project title]**

[2-3 sentences: the question you're trying to answer, what you've built so far, and what comes next. Example: extending my multi-object detector to instance segmentation by prompting SAM with Grounding DINO boxes, and measuring how mask quality changes on cluttered scenes.]

[GitHub →](https://github.com/Varun-Ponugoti/REPO)

## 🤖 Selected Robotics and AI Projects

**Single and Multi-Object Recognition (CNN + YOLOv8)**

A recognition system for 73 real-world objects: EfficientNetB0 classifies single objects at 94.2% test accuracy, and a fine-tuned YOLOv8s finds and locates every object in multi-object images at 0.806 mAP50 and 12 ms per image. Includes a leakage-free grid dataset built from single-object photos and auto-labeled with Grounding DINO.

[GitHub →](https://github.com/Varun-Ponugoti/DLAI)

**Stereo-to-Mono Crossover for Visual SLAM**

At what point does a degraded stereo camera stop being worth it? I injected blur, occlusion, and other degradations into TUM-VI data, measured their effect on ORB-SLAM3, and trained a health monitor that detects degradation and switches from stereo to mono in real time. [Add your key result, e.g., accuracy.]

[GitHub →](https://github.com/Varun-Ponugoti/REPO)

**Dynamic Trajectory Replanning for a 7-DoF Manipulator**

Collision-free replanning around moving obstacles in PyBullet, using RRT-Connect, trajectory optimization, path rewiring, and custom bounding volumes, with an error-analysis framework to measure performance. [Add your key result.]

[GitHub →](https://github.com/Varun-Ponugoti/REPO)

**Autonomous Mobile Robot for Obstacle Avoidance**

A wheeled robot built from hardware to software: vision-based obstacle detection, a SLAM pipeline for goal-directed navigation, and PID motion control with real-time replanning.

[GitHub →](https://github.com/Varun-Ponugoti/REPO)

## 📄 Publication

**Vision Language Models for Human-Like Perception in Robotics: A Systematic and Comprehensive Survey** (under review)
A survey of how VLMs are designed, trained, optimized, and applied to robotic systems.

## 🛠️ Tools

Python · C++ · PyTorch · TensorFlow · ROS 2 · ORB-SLAM3 · YOLOv8 · PyBullet · MuJoCo · Gazebo · Jetson Orin · SolidWorks

## 📫 Connect

[LinkedIn](https://linkedin.com/in/varunponugoti) · ponugoti.va@northeastern.edu
