# 딥러닝 기초 실습 — 빅데이터응용및보안 (2025년 2학기)

중부대학교 정보보호학전공 수업에서 Google Colab과 TensorFlow/Keras로 진행한 딥러닝 실습입니다.
이후 PyTorch로 진행한 병리 영상 분류 실험은 [pathology-tissue-classification](https://github.com/8woo4/pathology-tissue-classification)에 있습니다.

## 실습 목록

| 노트북 | 내용 | 모델 | 결과 |
|---|---|---|---|
| [mnist_dl.ipynb](mnist_dl.ipynb) | MNIST 손글씨 숫자 10종 분류, 맞힌/틀린 이미지 시각화 | 다층 신경망 (Dense 512-256-10) | 테스트 정확도 **98.76%** |
| [corona_sgd.ipynb](corona_sgd.ipynb) | 코로나 일일 확진자 시계열 예측 | SimpleRNN, optimizer **SGD** | 테스트 RMSE **331.63** |
| [corona_adam.ipynb](corona_adam.ipynb) | 같은 실험에서 optimizer만 변경 | SimpleRNN, optimizer **Adam** | 테스트 RMSE **177.87** |

## 정리

- **MNIST**: 학습 정확도는 100%, 테스트 정확도는 98.76%로 학습 데이터에 약간 과적합된 모습을 확인했습니다. 학습 점수가 아니라 테스트 점수로 성능을 판단해야 하는 이유를 체감했습니다.
- **코로나 예측**: 다른 조건은 그대로 두고 최적화 기법만 SGD에서 Adam으로 바꿨더니 테스트 RMSE가 331.63에서 177.87로 줄었습니다. 한 번에 하나만 바꿔야 결과 차이의 원인을 말할 수 있다는 것을 배웠습니다.

## 환경
Python, TensorFlow/Keras, scikit-learn, pandas, Google Colab
