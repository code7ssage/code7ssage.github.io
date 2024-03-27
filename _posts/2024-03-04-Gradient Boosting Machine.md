---
layout: post
title: Gradient Boosting Machine
---

- **Classification 뿐만 아니라 Regression 사용 가능**
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108130715.png?raw=true)
	- residual을 최소화 하는게 목적!
- [Overfitting](https://code7ssage.github.io/Overfitting/)문제..
	1. **Subsampling** 가능 
	- 복원 추출이 아닌(without replacement) Just sampling 하여 iteration 마다 data를 Sampling 하게 함 
	- 하지만 bagging (Bootstrap + Aggregating)도 또한 가능함
	2. **Shrinkage** 
	- Using for Reduction/Shrinking the impact of each additional fitted base-leaners (Penalty Term이랑  반대, λ(0~1)값이 작을 수록 validation error가 줄어듦) 
	- Better to improve a model by taking many **small steps than by taking fewer large steps**
		![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108131346.png?raw=true)
	3. **Early stopping**
-  Feature Importance Score
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108131701.png?raw=true)
	- L이 terminal nodes라고 할 때, L-1 splits, IG: imformation gain
- Step 1
	- Tree가 아닌 하나의 leaf (Single leaf) 부터 시작함 → 이 leaf는 Target(Y) 값에 대한 초기 추정 값을 나타냄 
	- GBM은 **Single leaf** 부터 시작하며, 그 single leaf 모델이 예측하는 Target(Y) **추정 값은 모든 Target의 평균 값으로 Setting 함**
	- 즉 첫번째 residual은 target-평균
- Step 2
	 - Residual(잔차)을 예측하는 Decision Tree를 Modeling 함 
	 - Terminal Node에 두 개 이상의 Residual 값이 있는 경우 평균으로 치환하여 넣어주게 됨
		![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108132031.png?raw=true)
- Step 3
	- Average Weight (Sigle leaf) + Predicted Residual 
	- 이렇게 하게 되면 1개의 Tree로 Residual이 거의 0으로 수렴하기 때문에 Overfitting이 일어날 수 있음
- Step 4
	- Overfitting을 방지하기 위해 Shrinkage(Learning Rate)을 사용함 → 학습한 Residual을 조금만 반영하겠다는 의미 (Penalty) 
	- Shrinkage (Learning Rate) = 0 ~ 1
		![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108132256.png?raw=true)
- Step 5
	- Residual update
	- residual의 절댓값이 줄어듦
		![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108132506.png?raw=true)
- Step N
	- new decisicion tree 만들어서 다시 residual update 반복 해주면 됨!
		![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240108132657.png?raw=true)
- 실습: [9. Gradient Boosting Machine Code](https://code7ssage.github.io/9.-Gradient-Boosting-Machine-Code/)