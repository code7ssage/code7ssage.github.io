---
title: LASSO Regression
---

- Least Absolute Shrinkage and Selection Operator 
- **|β|** = **𝑳𝟏−𝑛𝑜𝑟𝑚** = 𝑳𝟏 Regularization 에 Penalty Term을 부여하는 방식
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104144805.png?raw=true)
- MSE Contour: 중심에서 멀어질수록 Error([MSE](https://code7ssage.github.io/MSE/)) 증가 → Train Error를 조금 증가시키는 과정 ([Overfitting](https://code7ssage.github.io/Overfitting/)방지) 
- Lasso Estimator와 MSE Contour가 만나는 점이 제약 조건을 만족하며 Error가 최소가 됨
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104144912.png?raw=true)
- Ridge Regression과 달리 Lasso Formulation은 Closed Form Solution을 구하는 것이 불가능
- Numerical Optimization Methods 필요
	[Gradient Descent](https://code7ssage.github.io/Gradient-Descent/) 사용
- 예측에 중요하지 않은 변수가 더 빠르게 감소, t가 작아짐에 따라 예측에 중요하지 않은 변수는 0이 됨
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104145513.png?raw=true)
