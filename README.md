# NumPy 기반 Transformer Inference

## 프로젝트 개요

이 프로젝트는 Transformer 구조를 직접 이해하기 위해 PyTorch나 TensorFlow 같은 고수준 딥러닝 프레임워크 없이, NumPy를 활용해 Transformer inference 과정을 구현한 학습 프로젝트입니다.

단순히 모델을 사용하는 것에서 나아가, 입력 데이터가 embedding, attention, feed forward layer, token generation 과정을 거쳐 출력으로 이어지는 흐름을 직접 코드로 확인하는 것을 목표로 했습니다.

## 주요 구현 내용

- NumPy 기반 Transformer inference 구현
- Token embedding 및 positional encoding 구조 확인
- Self-Attention 연산 구현
- Q, K, V projection 흐름 분석
- Attention score 계산 과정 구현
- Feed Forward Network 구조 구현
- Layer Normalization 및 residual connection 흐름 확인
- Token generation 과정 실험

## 사용 기술

- Python
- NumPy
- Jupyter Notebook
- Google Colab

## 프로젝트 구조

```text
only_numpy_Transformer_inference
└── only_numpy_Transformer_inference.ipynb
```

## 실행 방법

1. 레포지토리를 클론합니다.

```bash
git clone https://github.com/juneddoha/only_numpy_Transformer_inference.git
cd only_numpy_Transformer_inference
```

2. Jupyter Notebook 또는 Google Colab에서 노트북을 실행합니다.

```bash
jupyter notebook only_numpy_Transformer_inference.ipynb
```

3. 노트북의 셀을 순서대로 실행하며 Transformer inference 흐름을 확인합니다.

## 학습 포인트

이 프로젝트를 통해 다음 내용을 학습했습니다.

- Transformer의 기본 구조
- Self-Attention에서 Q, K, V가 사용되는 방식
- Attention score가 계산되고 output으로 이어지는 과정
- Feed Forward Network와 Layer Normalization의 역할
- 고수준 라이브러리 없이 NumPy 연산만으로 모델 내부 흐름을 구현하는 방식

## 한계 및 개선 방향

현재 프로젝트는 Transformer 구조 학습을 위한 구현 중심 프로젝트입니다.  
추후 개선한다면 다음 내용을 추가할 수 있습니다.

- 코드 모듈화
- 실행 결과 예시 추가
- attention score 시각화
- FP32 / INT8 inference 비교
- README에 단계별 설명 이미지 추가
