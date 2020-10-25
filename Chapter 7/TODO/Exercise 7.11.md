## Exercise 7.11

### Question:

근사적 행동 가치가 변하지 않는다면, 트리 보강 이득(식 7.16)이 다음과 같이 기댓값에 기반한 TD 오차의 합으로 표현될 수 있음을 보여라.

![equation](https://latex.codecogs.com/svg.latex?G_{t:t&plus;n}&space;=&space;Q(S_t,&space;A_t)&space;&plus;&space;\sum_{k=t}^{min(t&plus;n-1,&space;T-1)}&space;\delta_k&space;\prod_{i=t&plus;1}^k&space;\gamma&space;\pi(A_i&space;|&space;S_i))

여기서 ![equation](https://latex.codecogs.com/svg.latex?\delta_t&space;\doteq&space;R_{t&plus;1}&space;&plus;&space;\gamma&space;\bar{V}_t(S_{t&plus;1})&space;-&space;Q(S_t,&space;A_t)) 이고, ![equation](https://latex.codecogs.com/svg.latex?\bar{V}_t) 는 식 7.8로부터 주어진다.

### Answer:
