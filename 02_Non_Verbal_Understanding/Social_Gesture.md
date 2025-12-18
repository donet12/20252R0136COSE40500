# SocialGesture: Delving into Multi-person Gesture Understanding

**[Paper Info]** CVPR 2025

## 1. Motivation
기존 제스처 인식 데이터셋들은 대부분 **"한 사람이 카메라를 보고 하는(One-person)"** 형태였습니다.
하지만 실제 사회적 상호작용은 여러 사람이 섞여 있는 환경에서 발생합니다.

### 📉 기존 데이터셋의 한계
* **NVGesture / EgoGesture:** 독사진 위주, 상호작용 부재.
* **SocialGesture (Ours):** 다자간 상호작용, 제스처의 **주체(Subject)**와 **대상(Target)**이 존재함.

## 2. SocialGesture Benchmark
새롭게 구축된 데이터셋은 다음과 같은 특징을 가집니다.

| Feature | SocialGesture (Ours) | Existing Datasets |
| :--- | :--- | :--- |
| **Environment** | Multi-person (다자간) | Single-person (개인) |
| **Interaction** | Subject ↔ Target | Subject Only |
| **Gesture Types** | Pointing, Showing, Giving, Reaching | Generic Gestures |
| **Annotation** | Bounding Box + Relationship | Label Only |

## 3. Tasks Breakdown
모델이 해결해야 할 3단계 과제입니다.

1.  **Gesture Detection:** 현재 장면에서 사회적 제스처가 발생했는가? (Yes/No)
2.  **Gesture Type Classification:** 어떤 종류의 제스처인가? (Pointing / Showing / Giving / Reaching)
3.  **Gesture Localization:**
    * **Subject:** 누가 제스처를 했는가? (BBox)
    * **Target:** 누구/무엇을 향했는가? (BBox)

## 4. Annotation Pipeline
GPT-4o와 인간 검수자를 결합한 효율적인 파이프라인을 구축했습니다.
* **Video Input** -> **GPT-4o Generation** -> **Three-person Consensus (사람 검수)** -> **Final Label**