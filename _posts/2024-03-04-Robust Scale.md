---
title: Robust Scale
categories:
  - key_terms
---

### Robust Scaler (로버스트 정규화)

- **동작 원리**: 중앙값(median)과 [사분위수(IQR)](https://code7ssage.github.io/key_terms/사분위수(IQR)/)를 사용하여 스케일링합니다. 이 방법은 이상치에 영향을 적게 받습니다.
- **수식**: {x−median(x)} / IQR(x)​ (IQR은 제3사분위수(Q3) - 제1사분위수(Q1))
- **적용 상황**: 데이터에 이상치가 많을 때 사용하는 것이 좋습니다