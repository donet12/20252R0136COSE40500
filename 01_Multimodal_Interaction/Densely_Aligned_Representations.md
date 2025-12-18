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
## 3. Tasks & Benchmarks

사회적 추론 게임인 'One Night Ultimate Werewolf'를 기반으로 3가지 태스크를 정의했습니다.

| Task | 설명 | 예시 상황 |
| :--- | :--- | :--- |
| Speaking Target ID | 청자 식별 | "너 거짓말 하고 있어"라고 할 때 시선이 향한 곳은? |
| Pronoun Coreference | 대명사 해소 | "He is a werewolf"에서 'He'는 누구인가? |
| Mentioned Player | 언급 대상 추론 | 이름이 생략되어도 문맥상 누구를 비난하고 있는가? |


## 4. Key Results

언어 모델(BERT) 단독 사용 시와 비교했을 때, 제안된 멀티모달 정렬 방식이 압도적인 성능 향상을 보였습니다.

- Language Model Only: 복잡한 상황(거짓말, 비꼬기 등)에서 맥락 파악 실패.
- Dense Alignment (Ours): 시각적 단서(눈맞춤, 손짓)를 결합하여 모호한 지칭 대상을 성공적으로 추론.