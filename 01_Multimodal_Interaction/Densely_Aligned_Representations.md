# Modeling Multimodal Social Interactions: Densely Aligned Representations

**Paper Info:** CVPR 2024 Oral

## 1. Problem Definition (연구 배경)

현실의 사회적 상호작용은 다자간(Multi-party)이며 멀티모달(Multimodal)입니다. 기존 모델들은 언어 모델과 시각 모델을 단순히 결합(Late Fusion)하는 수준에 그쳐, "누가(Who) 누구에게(To Whom) 무엇을(About Whom)" 말하는지 정확히 파악하지 못했습니다.

## 2. Methodology: Densely Aligned Fusion

본 연구는 시간 축에 따라 언어와 시각 정보를 정밀하게 매칭하는 Dense Alignment를 제안합니다.

### ⚙️ Model Pipeline Concept

1. Visual Cue Tracking: 화자의 얼굴, 시선, 제스처 키포인트를 프레임 단위로 추적 ($t=1$ to $T$).
2. Language Tokenization: 대화 내용을 토큰화하고, `[MASK]` 토큰을 활용해 예측 대상을 설정.
3. Dense Alignment (핵심):
   > Visual Features (Keypoints) ⟺ Language Context (Utterances)
   >
   > *시각적 제스처의 타이밍과 발화의 타이밍을 동기화하여 상호 참조 관계 학습*
