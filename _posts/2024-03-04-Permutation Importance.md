---
title: Permutation Importance
---

Permutation Feature Importance(순열 특성 중요도)는 머신러닝 모델에서 각 특성(feature)이 예측에 얼마나 중요한지를 평가하는 방법입니다. 이 방법은 모델이 이미 학습된 후에 적용됩니다. 순열 특성 중요도를 구하는 과정은 다음과 같습니다:

1. **모델 학습**: 먼저, 모든 특성을 사용하여 모델을 학습시킵니다.
    
2. **성능 측정**: 학습된 모델의 성능을 측정합니다. 이 성능은 기준점(baseline)으로 사용됩니다. 성능 측정 지표는 분류 문제의 경우 정확도나 ROC-AUC가 될 수 있고, 회귀 문제의 경우 MSE나 R²가 될 수 있습니다.
    
3. **특성 순열**: 하나의 특성에 대해, 테스트 세트 내의 데이터 포인트의 값을 무작위로 섞습니다(순열). 이렇게 하면 해당 특성의 데이터 구조가 파괴됩니다.
    
4. **성능 재측정**: 순열된 특성을 가진 데이터로 모델의 성능을 다시 측정합니다.
    
5. **중요도 계산**: 원래 성능에서 순열 후의 성능을 빼서 특성의 중요도를 계산합니다. 성능 저하가 클수록 해당 특성이 모델에 더 중요하다는 것을 의미합니다.
    
6. **반복**: 모든 특성에 대해 위 과정을 반복하여 각 특성의 중요도를 평가합니다.
    

### 장점:

- 모델에 종속적이지 않아 다양한 유형의 머신러닝 모델에 적용할 수 있습니다.
- 특성 중요도의 해석이 직관적입니다.
- 데이터의 실제 분포와 상관성을 반영하여 특성의 중요도를 평가합니다.

### 단점:

- 계산 비용이 많이 들 수 있습니다(특히 특성 수가 많거나 데이터 세트가 큰 경우).
- 데이터의 무작위 순열로 인해 노이즈가 발생할 수 있습니다.