---
layout: post
title: undersampling
---

- 데이터 내 클래스 비율이 Imbalance 할 경우, 타겟의 모수가 많은 쪽을 줄이는 기법 
- Random, Near Miss, Tomek Links, ENN 등 
- **Random Undersampling**은 지정한 종속변수의 Category 중 비율이 적은 Category를 기준으로 비율이 높은 Category의 데이터를 Random한 방법으로 제거 
- **Near Miss Undersampling**은 Near-Miss 알고리즘을 사용하여 데이터를 제거하는 방법 제거할 대상을 선정하기 위해 이웃한 근접 데이터 간의 거리를 계산하기 때문에 오래 걸림 
- [Tomek Links](https://code7ssage.github.io/Tomek-Links/)는 데이터의 중심 분포를 거의 유지하면서 분류 경계를 조정하기 때문에 제거되는 샘플이 한정적임 → Undersampling의 효과가 낮음 
- [ENN](https://code7ssage.github.io/ENN/)(Edited Nearest Neighbours) 는 다수 클래스 데이터 중 가장 가까운 (Nearest Neighbours)  k개의 데이터가 모두 다수 클래스가 아니면 삭제하는 방법                                                         