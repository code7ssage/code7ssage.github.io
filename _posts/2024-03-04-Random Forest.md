---
layout: post
title: Random Forest
---

- A specialized bagging for **decision tree algorithm**
- **Two ways** to increase the diversity of ensemble
	1. Bootstrap(복원추출) -> **Bagging**
	2. X% sampling -> **Randomly chosen predictor variables**
- 목표: Bias는 유지하면서 Variance를 낮춤
	• Tree는 작은 Bias와 큰 Variance를 갖기 때문에, 매우 깊이 성장한(Depth가 깊은) 트리는 훈련 데이터에 대해 [Overfitting](https://code7ssage.github.io/Overfitting/) 하게 됨 
	• 한 개의 Tree의 경우 훈련 데이터에 있는 **Noise**에 대해 매우 민감함 
	• Tree들이 서로 상관화(correlated)되어 있지 않다면 여러 Tree들의 평균은 Noise에 대해 강인해짐 
	• 상관화를 줄이는 방법은 **Randomly Chosen (행 & 렬 모두)**
	• 반면, Forest를 구성하는 모든 Tree들을 동일한 데이터 셋으로만 훈련시키게 되면, Tree들의 상관성은 커짐 -> **Bagging**은 서로 다른 데이터 셋들에 대해 훈련
- But, Bootstrap을 진행하면 확률 상 뽑히지 못한 데이터는 **36.8%** 가 됨
	-> 이 36.8%를 train set으로 활용: **OOB**(Out Of Bag) ㅇata
- **Feature Importance Score**
	Step 1 : original OOB data를 사용하여 error 측정
	Step 2 : OOB data의 변수 Xi를 permutation 시킨다 
	Step 3 : permutation시킨 OOB에 대해 error 측정하고 original과 비교한다
	- error의 증가량이 작다-> Xi는 별로 중요하지 않은 변수
	- error의 증가량이 크다-> Xi는 중요한 변수
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240106164456.png?raw=true)
	- di는 편차, si는 분산
		-> error의 차이는 크고, 그 큰 차이가 비슷하게 나타나야 함
- 실습: [7. Random Forest Code](https://code7ssage.github.io/7.-Random-Forest-Code/)