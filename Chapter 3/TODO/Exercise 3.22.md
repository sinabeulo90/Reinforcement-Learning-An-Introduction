## Exercise 3.22

### Question:

오른쪽 그림의 연속되는 MDP를 생각해 보자. '왼쪽'과 '오른쪽'의 두 가지 행동 선택만 가능한 맨 위에 있는 상태에서 내리는 결정이 유일한 결정이다. 숫자는 각 행동 이후에 이미 정해진 대로 받게 되는 보상을 나타낸다. 정확히 두 개의 결정론적 정책 ![equation](https://latex.codecogs.com/svg.latex?\pi_\text{left}) 과 ![equation](https://latex.codecogs.com/svg.latex?\pi_\text{right}) 이 존재한다.  ![equation](https://latex.codecogs.com/svg.latex?\gamma=0,0.9,0.5) 인 각 경우에 대해 어떤 정책이 가장 최적인가?

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;\pi_{left}&space;:&space;G_t&space;&=&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;G_{t&plus;1}&space;\\&space;&=&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;R_{t&plus;2}&space;&plus;&space;\gamma^2&space;G_{t&plus;2}&space;\\&space;&=&space;1&space;&plus;&space;\gamma^2&space;G_{t&plus;2}&space;\\&space;&=&space;1&space;&plus;&space;\gamma^2&space;&plus;&space;\gamma^4&space;&plus;&space;\cdots&space;&plus;&space;\gamma^{2i}&space;G_{t&plus;2i}&space;\\&space;&=&space;\frac{1}{1-\gamma^2}&space;\\&space;\pi_{right}&space;:&space;G_t&space;&=&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;G_{t&plus;1}&space;\\&space;&=&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;R_{t&plus;2}&space;&plus;&space;\gamma^2&space;G_{t&plus;2}&space;\\&space;&=&space;0&space;&plus;&space;2\gamma&space;&plus;&space;\gamma^2&space;G_{t&plus;2}&space;\\&space;&=&space;2\gamma&space;&plus;&space;2\gamma^3&space;&plus;&space;\cdots&space;&plus;&space;2\gamma^{2i&plus;1}&space;G_{t&plus;2i&plus;1}&space;\\&space;&=&space;\frac{2\gamma}{1-\gamma^2}&space;\\&space;\end{align*}" title="\begin{align*} \pi_{left} : G_t &= R_{t+1} + \gamma G_{t+1} \\ &= R_{t+1} + \gamma R_{t+2} + \gamma^2 G_{t+2} \\ &= 1 + \gamma^2 G_{t+2} \\ &= 1 + \gamma^2 + \gamma^4 + \cdots + \gamma^{2i} G_{t+2i} \\ &= \frac{1}{1-\gamma^2} \\ \pi_{right} : G_t &= R_{t+1} + \gamma G_{t+1} \\ &= R_{t+1} + \gamma R_{t+2} + \gamma^2 G_{t+2} \\ &= 0 + 2\gamma + \gamma^2 G_{t+2} \\ &= 2\gamma + 2\gamma^3 + \cdots + 2\gamma^{2i+1} G_{t+2i+1} \\ &= \frac{2\gamma}{1-\gamma^2} \\ \end{align*}" />

<br>

| ![equation](https://latex.codecogs.com/svg.latex?\gamma) | | ![equation](https://latex.codecogs.com/svg.latex?G_{\pi_{left}}) | ![equation](https://latex.codecogs.com/svg.latex?G_{\pi_{right}) | 설명 |
|:-:|:-:|:-:|:-:|:-:|
| 0 | | 1 | 0 | ![equation](https://latex.codecogs.com/svg.latex?\gamma<0.5) 인 경우, 최적 정책은 ![equation](https://latex.codecogs.com/svg.latex?\pi_{left}) |
| 0.9 | | 5.26 | 9.47 | ![equation](https://latex.codecogs.com/svg.latex?\gamma>0.5) 인 경우, 최적 정책은 ![equation](https://latex.codecogs.com/svg.latex?\pi_{right}) |
| 0.5 | | 1.33 | 1.33 | ![equation](https://latex.codecogs.com/svg.latex?\gamma=0.5) 인 경우, 최적 정책은 ![equation](https://latex.codecogs.com/svg.latex?\pi_{left},\pi_{right}) |