# RoomPilot Edge

> Indoor navigation and semantic mapping with local agent planning

## 1. Project Overview

**RoomPilot Edge** is a GitHub-ready project idea focused on **indoor semantic perception, navigation support, spatial AI, edge agents**.

Many indoor navigation systems depend on external infrastructure or cloud services. This project uses on-device vision to detect navigational landmarks, segment traversable areas, and answer navigation-oriented questions locally.

**Target area:** Snapdragon / Android edge AI  
**Primary users:** visually impaired users, indoor robotics researchers, smart-building prototypes

This repository is designed as a portfolio-grade edge AI project. The final target is **fully offline inference on a Snapdragon-powered Android device (for example, Galaxy S24 Ultra)**. When a larger model is mentioned, it is meant for the **desktop training/distillation/benchmark side**, while the shipped mobile app remains privacy-preserving and offline-first.

---

## 2. Why This Project Matters

This project shows the ability to think across:

- model design
- optimization and quantization or systems tuning
- runtime constraints
- reproducible benchmarking
- product-style engineering and evaluation


---

## 3. Core Features

- Detection of doors, stairs, desks, exits, signs, and obstacles
- Segmentation of floor, free space, walls, and blocked regions
- Lightweight semantic map construction from short camera sequences
- Offline agent that answers queries such as 'where is the exit?' or 'is the path blocked?'
- Session-based memory for repeated indoor routes

---

## 4. Proposed System Architecture

1. Camera frames are sampled and stabilized
2. Objects and free-space regions are inferred on-device
3. Semantic map stores landmarks and traversable directions
4. Agent consults current observations + recent map memory
5. UI presents text, icons, or optional voice output

---

## 5. Recommended Tech Stack

- Android + CameraX
- Mobile-friendly detectors and segmenters
- Simple map graph or scene-memory module
- Local LLM/VLM or rule-based planner
- Optional IMU fusion for more robust movement estimation


---

## 6. Data / Workload Ideas

ADE20K subsets, ScanNet labels, indoor navigation datasets, and custom room walkthrough clips.

For a strong repository, keep one **small reproducible benchmark set** in the repo and document how the larger benchmark was prepared. That makes the project easier for others to run and review.

---

## 7. Milestone Plan

### Phase 1
Implement landmark detection and free-space segmentation

### Phase 2
Create a lightweight map-memory abstraction

### Phase 3
Build navigation question-answer flow

### Phase 4
Stress-test in hallways, classrooms, and offices

### Phase 5
Optimize memory, latency, and output clarity

### Final Deliverable
A working demo, a benchmark report, and clear ablations showing what changed performance or accuracy.

---

## 8. Evaluation Metrics

- Landmark detection accuracy
- Free-space IoU
- Route suggestion correctness on test scenarios
- Agent answer relevance
- Memory and battery usage over multi-minute sessions


A great final report should include:

- baseline vs optimized comparison
- error analysis
- failure cases
- hardware/runtime notes
- screenshots or short demo GIFs

---

## 9. Suggested Repository Structure

```text
roompilot-edge/
├── README.md
├── app/ or src/
├── models/
├── scripts/
├── configs/
├── notebooks/ or reports/
├── benchmarks/
├── assets/
└── docs/
```

---
