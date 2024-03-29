---
title: Gradient Descent
---

- 경사 하강법 
- Non-convex 경우 Gradient Descent를 활용하여 해(Loss가 가장 낮은)를 찾아 감
- 대부분의 non-linear regression 문제는 closed form solution이 존재하지 않음 
- Closed form solution이 존재해도 수많은 parameter가 있을 때 Gradient Descent로 해결하는 것이 효율적
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104145217.png?raw=true)
- Local Minima에 빠질 수 있음 
- 우리는 Global Minimum이 있는지 알 수 없음
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104145300.png?raw=true)
- Local Minima에서 빠져나오기 위해 Momentum이라는 변수를 사용함 
- 어느정도 하강 시 다른 곳으로 툭 튀어 버리게 되면서 Local Minima를 빠져나옴
	![image](https://github.com/code7ssage/code7ssage.github.io/blob/master/assets/attached%20file/Pasted%20image%2020240104145336.png?raw=true)