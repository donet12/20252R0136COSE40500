# Gaze-LLE: Gaze Target Estimation via Large-Scale Learned Encoders

**[Paper Info]** CVPR 2025 Highlight 🌟

## 1. TL;DR (핵심 요약)
복잡하고 무거운 보조 모델들(Depth, Pose, 3D Estimation)을 전부 제거하고, **Visual Foundation Model (DINOv2)** 하나만으로 시선 추적 성능을 극대화한 연구입니다.

## 2. The Problem: Complexity vs Efficiency
기존 시선 추적 모델들은 성능을 높이기 위해 너무 많은 것들을 붙였습니다.
* **기존 방식:** `Input Image` + `Depth Model` + `3D Pose Model` + `Face Detector` ...
* **문제점:** 연산량이 폭증하고, 하나의 서브 모델이 틀리면 전체 결과가 틀리는 오류 전파(Error Propagation) 발생.

