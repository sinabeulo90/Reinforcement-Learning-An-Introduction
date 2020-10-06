## Exercise 3.24

### Question:

그림 3.5에 따르면 격자 공간에서 가장 좋은 상태의 최적 가치는 소수 첫째 자리까지 어림했을 때 24.4이다. 최적 정책에 대한 지식과 식 3.8을 이용하여 이 가치를 상징적으로 표현하고 소수 셋째 자리까지 계산하라.

### Answer:

가장 높은 가치를 가지는 상태에서부터 최적 정책에 따라 움직이면, A ⇒ A' ⇒ A의 최단거리 경로로 움직인다. 이 경로를 따라 연속적인 작업에서의 할인된 이득의 기대값을 구하면,

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;G_t&space;&=&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;R_{t&plus;2}&space;&plus;&space;\gamma^2&space;R_{t&plus;3}&space;&plus;&space;\gamma^3&space;R_{t&plus;4}&space;&plus;&space;\gamma^4&space;R_{t&plus;5}&space;&plus;&space;\cdots&space;\\&space;&=&space;10&space;&plus;&space;10&space;\gamma^5&space;&plus;&space;\cdots&space;\\&space;&=&space;10&space;\sum_{t=0}^\infty&space;\gamma^{5t}&space;\\&space;&=&space;\frac{10}{1-\gamma^5}&space;\end{align*}" title="\begin{align*} G_t &= R_{t+1} + \gamma R_{t+2} + \gamma^2 R_{t+3} + \gamma^3 R_{t+4} + \gamma^4 R_{t+5} + \cdots \\ &= 10 + 10 \gamma^5 + \cdots \\ &= 10 \sum_{t=0}^\infty \gamma^{5t} \\ &= \frac{10}{1-\gamma^5} \end{align*}" />

<br>

![equation](https://latex.codecogs.com/svg.latex?\gamma=0.9) 이므로, ![equation](https://latex.codecogs.com/svg.latex?G_t=24.419) 가 된다.