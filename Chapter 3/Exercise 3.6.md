## Exercise 3.6

### Question:

막대 균형 잡기 작업을 에피소딕 작업으로 다루지만 할인도 이용한다고 가정해 보자. 실패에 대한 보상은 -1이고 그 밖의 보상은 0이다. 이때 매 순간의 이득은 무엇인가? 이 이득은 할인을 이용한 연속적인 작업 형식에서의 이득과 어떻게 다른가?

### Answer:

실패에 대한 보상이 -1이고 그 밖의 보상은 0일 때, 할인을 이용하는 에피소딕 작업의 매 순간의 이득을 계산하면,

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;G_t&space;&\doteq&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;R_{t&plus;2}&space;&plus;&space;\gamma^2&space;R_{t&plus;3}&space;&plus;&space;\cdots&space;&plus;&space;\gamma^{T-t-1}&space;R_T&space;\\&space;&=&space;0&space;&plus;&space;0&space;&plus;&space;0&space;&plus;&space;\cdots&space;&plus;&space;\gamma^{T-t-1}&space;(-1)&space;\\&space;&=&space;-\gamma^{T-t-1}&space;\end{align*}" title="\begin{align*} G_t &\doteq R_{t+1} + \gamma R_{t+2} + \gamma^2 R_{t+3} + \cdots + \gamma^{T-t-1} R_T \\ &= 0 + 0 + 0 + \cdots + \gamma^{T-t-1} (-1) \\ &= -\gamma^{T-t-1} \end{align*}" />

이므로, 매 순간의 이득은 ![equation](https://latex.codecogs.com/svg.latex?-\gamma^{T-t-1}) 이 된다.

이 이득은 종단 시각 ![equation](https://latex.codecogs.com/svg.latex?T) 는 유한한 값을 가진다는 것을 제외하면 연속적인 작업의 형식과 동일하다.
