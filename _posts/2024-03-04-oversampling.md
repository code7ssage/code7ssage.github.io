---
title: oversampling
categories:
  - key_terms
---

- 데이터내클래스비율이 Imbalance 할 경우, 타겟의 모수가 많은쪽을줄이는기법(Random, SMOTE 등) 
- **Random**은 Undersampling과 반대로 비율이 낮은 데이터를 Random으로 복제하여 데이터의양을 늘림 
- [SMOTE](https://code7ssage.github.io/SMOTE/)(Synthetic Minority Oversampling Technique)은 무작위로 선택한데이터에 KNN을수행, 수행한 X(KNN)와 X의사이에위치한가상의데이터를생성 