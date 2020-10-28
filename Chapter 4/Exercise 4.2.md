## Exercise 4.2

### Question:

예제 4.1에서, 새로운 상태 15가 격자 공간에서 상태 13 바로 아래에 추가되고 left, up, right, down의 행동이 에이전트를 12, 13, 14, 15의 상태로 각각 이동시킨다고 가정해보자. 원래 주어졌던 상태에서 '시작하는' 전이는 변하지 않는다고 가정하자. 그러면 균일한 확률을 갖는 무작위 정책에 대해 ![equation](https://latex.codecogs.com/svg.latex?v_\pi(15)) 의 값은 얼마인가? 이제 상태 13의 동역학도 변해서 상태 13으로부터 행동 down을 하면 제이전트가 새로운 상태 15로 이동한다고 해 보자. 이 경우 균일한 확률을 갖는 무작위 정책에 대해 ![equation](https://latex.codecogs.com/svg.latex?v_\pi(15)) 의 값은 얼마인가?

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;v_\pi(15)&space;&=&space;\sum_a&space;\pi(a|15)&space;\sum_{s',r}[r&space;&plus;&space;v_\pi(s')]&space;\\&space;&=&space;0.25(-1&space;-22)&space;&plus;&space;0.25(-1&space;-20)&space;&plus;&space;0.25(-1&space;-14)&space;&plus;&space;0.25(-1&space;&plus;&space;v_\pi(15))&space;\\&space;&=&space;-15&space;&plus;&space;0.25v_\pi(15)&space;\\\\&space;v_\pi(15)&space;&=&space;-15/0.75&space;=&space;-20&space;\end{align*}" title="\begin{align*} v_\pi(15) &= \sum_a \pi(a|15) \sum_{s',r}[r + v_\pi(s')] \\ &= 0.25(-1 -22) + 0.25(-1 -20) + 0.25(-1 -14) + 0.25(-1 + v_\pi(15)) \\ &= -15 + 0.25v_\pi(15) \\\\ v_\pi(15) &= -15/0.75 = -20 \end{align*}" />

상태 13의 동역학이 새로운 상태 15로 이동하는 경우를 포함하더라도, ![equation](https://latex.codecogs.com/svg.latex?v_\pi(13)) 의 값은 변하지 않으므로, ![equation](https://latex.codecogs.com/svg.latex?v_\pi(15)=15) 이다.

[Ch 4.1 testbed.ipynb](./Ch%204.1%20testbed.ipynb)
