---
title: ElasticNet
categories:
  - key_terms
toc: true
---

- ElasticNet은 Ridge의 𝑳𝟏−𝑛𝑜𝑟𝑚 과 LASSO의 𝑳𝟐−𝑛𝑜𝑟𝑚 을 섞어 놓았음
- λ𝟏 : LASSO Penalty Term (Feature Selection) 
- λ𝟐 : Ridge Penalty Term ([다중공선성](https://code7ssage.github.io/key_terms/다중공선성/) 방지) 
- ElasticNet은 Correlation이 강한 변수를 동시에 선택/배제하는 특정을 가지고 있음
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104145931.png?raw=true)
- 일정 범위 내로 λ𝟏, λ𝟐 를 조정하여, 가장 좋은 예측 결과를 보이는 λ𝟏, λ𝟐를 선정함 
- Ridge, LASSO 보다 더 많은 실험이 필요하다는 단점이 존재함
- **해공간**
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104150051.png?raw=true)
