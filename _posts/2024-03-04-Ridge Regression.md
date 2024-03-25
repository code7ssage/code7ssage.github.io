---
layout: post
title: Ridge Regression
---

- β^𝟐에 Penalty Term을 부여하는 방식 
- β^2= **𝑳𝟐−𝑛𝑜𝑟𝑚** = 𝑳𝟐 Regularization
- Penalty Term을 추가한 **Regularized Model의 경우 Feature 간 Scaling이 필수**
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104143700.png?raw=true)
- **hyperparameter(λ)** 값 조절 
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104143843.png?raw=true)
- MSE Contour: 중심에서 멀어질수록 Error([[2024-03-04-MSE]]) 증가 → Train Error를 조금 증가시키는 과정 ([[2024-03-04-Overfitting]]방지) 
- Ridge Estimator와 MSE Contour가 만나는 점이 제약 조건을 만족하며 Error가 최소가 됨
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104144127.png?raw=true)
- Ridge는 미분이 가능하기 때문에 **Closed Form solution**을 구할 수 있음 
- 빠르게 해를 찾을 수 있다는 장점이 있음
- Ridge는 해 공간에서도 볼 수 있듯 **Feature Selection은 되지 않음** 
- 하지만 불필요한 Feature는 충분히 0에 거의 수렴하게 만들어 버림 
- Ridge Regression은 Feature의 크기가 결과에 큰 영향을 미치기 때문에 Scaling이 중요함 
- [[2024-03-04-다중공선성]](Multicollinearity) 방지에 가장 많이 쓰임
- 크기가 큰 변수가 더 빠르게 감소하는 경향을 보임
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104145550.png?raw=true)