---
layout: post
title: combination sampling
---

- 실전에서는 역시 한가지 방법만 시도하지 않음 
- SMOTEENN, SMOTETOMEK 등 
- **SMOTEENN**은 [[2024-03-25-SMOTE]](Over) 방법과 [[2024-03-25-ENN]](Under)을 조합하는 방법 
    → SMOTE를 통해 소수 클래스 데이터를 Oversampling하고 ENN을 통해 다수 클래스의 데이터를 Undersampling하는 방법 
- **SMOTETOMEK** → [[2024-03-25-SMOTE]]를 통해 소수 클래스 데이터를 Oversampling하고 [[2024-03-25-Tomek Links]]를 통해 다수 클래스의 데이터를 Undersampling하는 방법→ TOMEK의 특성으로 인해 결정 경계가 뚜렷해짐