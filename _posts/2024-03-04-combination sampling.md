---
layout: post
title: combination sampling
---

- 실전에서는 역시 한가지 방법만 시도하지 않음 
- SMOTEENN, SMOTETOMEK 등 
- **SMOTEENN**은 [SMOTE](https://code7ssage.github.io/SMOTE/)(Over) 방법과 [ENN](https://code7ssage.github.io/ENN/)(Under)을 조합하는 방법 
    → SMOTE를 통해 소수 클래스 데이터를 Oversampling하고 ENN을 통해 다수 클래스의 데이터를 Undersampling하는 방법 
- **SMOTETOMEK** → [SMOTE](https://code7ssage.github.io/SMOTE/)를 통해 소수 클래스 데이터를 Oversampling하고 [Tomek Links](https://code7ssage.github.io/Tomek-Links/)를 통해 다수 클래스의 데이터를 Undersampling하는 방법→ TOMEK의 특성으로 인해 결정 경계가 뚜렷해짐