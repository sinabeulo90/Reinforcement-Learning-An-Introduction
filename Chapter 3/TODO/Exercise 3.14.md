## Exercise 3.14

### Question:

예제 3.5의 그림 3.2에서 오른쪽 그림에 보이는 가치 함수 ![equation](https://latex.codecogs.com/svg.latex?v_\pi) 를 구하기 위한 벨만 방정식(식 3.14)은 모든 상태에 대해 만족해야 한다. +2.3, +0.4, -0.4, +0.7의 가치(이 숫자들은 오직 소수점 첫째 자리까지 정확하다)를 갖는 이웃한 네 개의 상태와 관련하여 +0.7의 가치를 갖는 중앙 상태가 이 방정식을 만족시킨다는 것을 수치적으로 보여라.

### Answer:

에이전트가 모든 상태에서 동일한 확률로 네 가지 행동 중 하나를 선택하므로 ![equation](https://latex.codecogs.com/svg.latex?\pi(a|s)=0.25)이고, 0.7의 가치를 갖는 중앙 상태에서 어떤 방향으로 움직이던 받는 보상은 0이다.

![equation](https://latex.codecogs.com/svg.latex?\gamma=0.9)인 할인된 보상을 이용할 경우, 벨만 방적식으로 중앙 상태의 가치를 계산하면,

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;v_\pi(s)&space;&=&space;\sum_{a}&space;\pi(a|s)&space;\sum_{s',&space;r}&space;p(s',r|s,a)&space;[r&space;&plus;&space;\gamma&space;v_pi(s')]&space;\\&space;&=&space;0.25&space;\cdot&space;[0&space;&plus;&space;0.9&space;\cdot&space;2.3]&space;&plus;&space;0.25&space;\cdot&space;[0&space;&plus;&space;0.9&space;\cdot&space;0.4]&space;\\&space;&\quad&space;&plus;&space;0.25&space;\cdot&space;[0&space;&plus;&space;0.9&space;\cdot&space;(-0.4)]&space;&plus;&space;0.25&space;\cdot&space;[0&space;&plus;&space;0.9&space;\cdot&space;0.7]&space;\\&space;&=&space;0.25&space;\cdot&space;0.9&space;\cdot&space;[0.23&space;&plus;&space;0.4&space;-&space;0.4&space;&plus;&space;0.7]&space;\\&space;&=&space;0.675&space;\end{align*}" title="\begin{align*} v_\pi(s) &= \sum_{a} \pi(a|s) \sum_{s', r} p(s',r|s,a) [r + \gamma v_pi(s')] \\ &= 0.25 \cdot [0 + 0.9 \cdot 2.3] + 0.25 \cdot [0 + 0.9 \cdot 0.4] \\ &\quad + 0.25 \cdot [0 + 0.9 \cdot (-0.4)] + 0.25 \cdot [0 + 0.9 \cdot 0.7] \\ &= 0.25 \cdot 0.9 \cdot [0.23 + 0.4 - 0.4 + 0.7] \\ &= 0.675 \end{align*}" />

따라서 소수점 둘째 자리에서 반올림하면 0.7의 가치를 가지므로, 중앙 상태의 가치와 일치한다.