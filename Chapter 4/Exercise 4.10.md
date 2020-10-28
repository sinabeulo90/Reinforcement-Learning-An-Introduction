## Exercise 4.10

### Question:

행동 가치 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;q_{k&plus;1}(s,a)) 에 대해서도 가치 반복 갱신(식 4.10)과 유사한 것이 있다면 무엇이겠는가?

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;q_{k&plus;1}(s,a)&space;&\doteq&space;\mathbb{E}[R_{t&plus;1}&space;&plus;&space;\max_{A_{t&plus;1}}&space;\gamma&space;q_k(S_{t&plus;1},A_{t&plus;1})&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\sum_{s',r}p(s',r|s,a)[r&plus;&space;\max_{a'}&space;\gamma&space;q_k(s',a')]&space;\end{align*}" title="\begin{align*} q_{k+1}(s,a) &\doteq \mathbb{E}[R_{t+1} + \max_{A_{t+1}} \gamma q_k(S_{t+1},A_{t+1}) | S_t=s, A_t=a] \\ &= \sum_{s',r}p(s',r|s,a)[r+ \max_{a'} \gamma q_k(s',a')] \end{align*}" />
