---
title: Matrix Factorization, Factorization Machine
categories:
  - key_terms
toc: true
---

### Matrix Factorization (행렬 분해)

행렬 분해는 큰 행렬을 더 작은 행렬들로 분해하는 과정입니다. 이 방법은 추천 시스템, 이미지 처리, 문서 분석 등 다양한 분야에서 사용됩니다. 가장 널리 알려진 예는 사용자의 상품에 대한 선호도를 예측하는 추천 시스템에서의 사용입니다. 예를 들어, 사용자-아이템 평가 행렬을 두 개의 낮은 차원의 행렬로 분해하여 사용자의 숨겨진 특성과 아이템의 특성을 추출합니다. 이렇게 추출된 특성을 기반으로 사용자가 아직 평가하지 않은 아이템에 대한 선호도를 예측할 수 있습니다.

### Factorization Machine (팩토리제이션 머신)

팩토리제이션 머신은 특히 sparsity가 있는 데이터셋에서 효과적인 예측 모델입니다. 이 기법은 특성 간의 모든 상호작용을 고려하여 예측을 수행합니다. 예를 들어, 사용자의 나이, 성별, 구매 이력과 같은 다양한 특성들이 있을 때, 이 특성들 간의 가능한 모든 조합을 고려하여 예측 모델을 만듭니다. 팩토리제이션 머신은 선형 회귀, SVM과 같은 다른 기계학습 알고리즘보다 더 복잡한 상호작용을 모델링할 수 있으며, 추천 시스템, 광고 예측, 텍스트 분류 등 다양한 분야에 적용됩니다.