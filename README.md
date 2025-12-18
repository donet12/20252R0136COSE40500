# Towards Socially-Intelligent AI: Modeling Human Social Interactions 🧠

> **Research Review based on:** Computers Colloquium - Prof. Sangmin Lee (Korea Univ, Pixel Lab)

## 📌 Overview

이 레포지토리는 Socially-Intelligent AI(사회적 지능을 가진 AI)를 구현하기 위한 핵심 연구들을 분석하고 정리한 아카이브입니다. 단순한 객체 인식을 넘어, 다자간 대화(Multi-party conversation) 상황에서 "눈치(Nunchi)"를 가진 AI를 만들기 위한 멀티모달 상호작용 기술을 다룹니다.

## 📚 Key Research Topics

### 1. [Multimodal Social Interactions](./01_Multimodal_Interaction/Densely_Aligned_Representations.md) (CVPR 2024 Oral)

- **주제:** 다자간 대화에서의 화자-청자 및 언급 대상 식별
- **핵심:** 언어(Verbal)와 시각(Non-verbal) 정보의 밀집 정렬(Dense Alignment)
- **데이터:** One Night Ultimate Werewolf (사회적 추론 게임)

### 2. [Social Gesture Understanding](./02_Non_Verbal_Understanding/Social_Gesture.md) (CVPR 2025)

- **주제:** 다수 인원 환경에서의 미세한 사회적 제스처 이해
- **핵심:** 기존 독사진 위주 데이터셋의 한계를 극복한 SocialGesture 벤치마크 구축
- **태스크:** 제스처 감지, 유형 분류, 주체(Subject) 및 대상(Target) 식별

### 3. [Gaze Target Estimation](./02_Non_Verbal_Understanding/Gaze_LLE.md) (CVPR 2025 Highlight)

- **주제:** 시선 추적(Gaze Following) 모델의 경량화 및 고도화
- **핵심:** Gaze-LLE. 거대 시각 모델(DINOv2)을 활용하여 복잡한 보조 모델 없이 SOTA 성능 달성

---

## 🚀 Future Direction: Belief Awareness

진정한 Social AI로 나아가기 위해서는 행동 관찰을 넘어 믿음(Belief)을 모델링해야 합니다.

1. **Individual Beliefs:** 각 개인이 가지고 있는 생각과 의도
2. **Shared Beliefs:** 사회적/문화적 규범(Norms)과 공유된 지식