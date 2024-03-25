---
layout: post
title: cross validation
---

- 결과에 대한 분산을 줄이기 위해 사용하는 기법 
    -> K-fold Cross validation이 대표적으로 많이 사용됨 
- K-fold Cross validation? 
    -> 전체 데이터를 K개의 fold로 나눔 
    -> fold간 데이터는 서로 겹치지 않게 나눠야 함
    ![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240103144045.png?raw=true)
- 4-fold cross validation
    ![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240103144141.png?raw=true)
- **StratifiedKFold**는 K-fold Cross validation에서 Label의 분포를 고려하지 않는 문제점을 보완한 Cross validation 기법 
    ->Class별 Label 분포를 고려하여 Fold를 나눠서 Fold 별 class 불균형을 해결
    ![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240103144323.png?raw=true)
