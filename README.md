README for only_numpy_Transformer_inference
NumPy 기반 Decoder-only Transformer Inference
프로젝트 개요

이 프로젝트는 Transformer 구조를 직접 이해하기 위해 PyTorch나 TensorFlow와 같은 고수준 딥러닝 프레임워크 없이 NumPy만으로 Decoder-only Transformer inference 과정을 구현한 학습 프로젝트입니다.

단순히 모델을 사용하는 것에서 나아가, 토큰화, 임베딩, Multi-Head Self-Attention, KV Cache, FFN, Layer Normalization, token generation이 어떤 순서로 동작하는지 직접 코드로 확인하는 것을 목표로 했습니다.

주요 구현 내용
Byte-level tokenizer 구현
Decoder-only Transformer 구조 구현
Multi-Head Self-Attention 구현
RoPE 기반 위치 정보 반영
KV Cache 기반 incremental decoding 구현
Layer Normalization, GELU, FFN 구현
Greedy decoding 및 top-k sampling 구현
NumPy 기반 weight 저장 및 로드 구조 구현
사용 기술
Python
NumPy
Jupyter Notebook
Google Colab
프로젝트 구조
only_numpy_Transformer_inference
└── only_numpy_Transformer_inference.ipynb
실행 방법
레포지토리를 클론합니다.
git clone https://github.com/juneddoha/only_numpy_Transformer_inference.git
cd only_numpy_Transformer_inference
Jupyter Notebook 또는 Google Colab에서 노트북을 실행합니다.
jupyter notebook only_numpy_Transformer_inference.ipynb
노트북의 셀을 순서대로 실행하여 Transformer inference 흐름을 확인합니다.
학습 포인트

이 프로젝트를 통해 다음 내용을 직접 확인했습니다.

Q, K, V projection이 attention 계산에 사용되는 방식
Head별 attention 계산 후 다시 하나의 벡터로 합쳐지는 과정
KV Cache가 이전 토큰의 Key/Value를 저장하여 반복 계산을 줄이는 방식
LayerNorm, residual connection, FFN이 decoder block 안에서 사용되는 흐름
Token generation 과정에서 logits, softmax, sampling이 연결되는 방식
한계 및 개선 방향

현재 프로젝트는 Transformer 구조 학습을 위한 구현 중심 프로젝트입니다.
추후 개선한다면 다음 내용을 추가할 수 있습니다.

README에 실행 결과 예시 이미지 추가
코드 모듈화
학습된 weight를 활용한 실제 문장 생성 실험
FP32 / INT8 inference 비교
attention score 시각화
간단한 튜토리얼 형태의 설명 문서 추가
