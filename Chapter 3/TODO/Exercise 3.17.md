## Exercise 3.17

### Question:

행동 가치, 다시 말해 ![equation](https://latex.codecogs.com/svg.latex?q_\pi) 에 대한 벨만 방정식은 무엇인가? 그 방정식은 상태-행동 쌍 ![equation](https://latex.codecogs.com/svg.latex?(s,&space;a)) 로부터 파생된 상태-행동 쌍의 행동 가치 ![equation](https://latex.codecogs.com/svg.latex?q_\pi(s',&space;a')) 으로부터 행동 가치 ![equation](https://latex.codecogs.com/svg.latex?q_\pi(s,&space;a)) 를 도출해야만 한다. 힌트: 오른쪽의 보강 다이어그램이 이 방정식에 해당한다. 행동 가치에 대해 식 3.14와 유사한 일련의 방정식을 보여라.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;q_\pi(s,&space;a)&space;&=&space;\mathbb{E}[G_t&space;|&space;S_t&space;=&space;s,&space;A_t&space;=&space;a]&space;\\&space;&=&space;\mathbb{E}[R_{t&plus;1}&space;&plus;&space;\gamma&space;G_{t&plus;1}&space;|&space;S_t&space;=&space;s,&space;A_t&space;=&space;a]&space;\\&space;&=&space;\sum_{s',r}&space;p(s',r|s,a)&space;[r&space;&plus;&space;\gamma&space;\mathbb{E}[G_{t&plus;1}&space;|&space;S_{t&plus;1}=s']]&space;\\&space;&=&space;\sum_{s',r}&space;p(s',r|s,a)&space;[r&space;&plus;&space;\gamma&space;v_\pi(s')]&space;\\&space;&=&space;\sum_{s',r}&space;p(s',r|s,a)&space;[r&space;&plus;&space;\gamma&space;\sum_{a'}&space;\pi(a'|s')&space;q_\pi(s',a')]&space;\end{align*}" title="\begin{align*} q_\pi(s, a) &= \mathbb{E}[G_t | S_t = s, A_t = a] \\ &= \mathbb{E}[R_{t+1} + \gamma G_{t+1} | S_t = s, A_t = a] \\ &= \sum_{s',r} p(s',r|s,a) [r + \gamma \mathbb{E}[G_{t+1} | S_{t+1}=s']] \\ &= \sum_{s',r} p(s',r|s,a) [r + \gamma v_\pi(s')] \\ &= \sum_{s',r} p(s',r|s,a) [r + \gamma \sum_{a'} \pi(a'|s') q_\pi(s',a')] \end{align*}" />