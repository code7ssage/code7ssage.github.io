---
title: Precision
categories:
  - key_terms
toc: true
---

### 정밀도 (Precision)

- **정의**: 모델이 True로 예측한 경우 중 실제로 True인 비율입니다.
- **계산**: 정밀도 = TP / (TP + FP)
    - TP(True Positive): 실제 True이며 모델도 True로 예측한 경우
    - FP(False Positive): 실제 False이지만 모델이 True로 잘못 예측한 경우
- **중요성**: 정밀도가 중요한 경우는 False Positive(거짓 양성) 결과를 최소화해야 할 때입니다. 예를 들어, 스팸 메일을 필터링할 때 실제로 중요한 메일을 스팸으로 분류하는 것을 피해야 하는 상황입니다.