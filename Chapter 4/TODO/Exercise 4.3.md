## Exercise 4.3

### Question:

행동 가치 함수 ![equation](https://latex.codecogs.com/svg.latex?q_\pi) 와 그것에 연이은 근사 함수 ![equation](https://latex.codecogs.com/svg.latex?q_0,q_1,q_2,\cdots) 에 대해 식 4.3, 식 4.4, 식 4.5와 유사한 방정식은 무엇인가?

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;q_\pi(s,a)&space;&\doteq&space;\mathbb{E}_\pi[G_t&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\mathbb{E}_\pi[R_{t&plus;1}&space;&plus;&space;\gamma&space;G_{t&plus;1}&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\mathbb{E}[R_{t&plus;1}&space;&plus;&space;\gamma&space;v_\pi(S_{t&plus;1})&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\mathbb{E}[R_{t&plus;1}&space;&plus;&space;\gamma&space;q_\pi(S_{t&plus;1},&space;A_{t&plus;1})&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\sum_{s',r}p(s',r|s,a)[r&space;&plus;&space;\gamma&space;\sum_{a'}\pi(a'|s')q_\pi(s',a')]&space;\\&space;q_{k&plus;1}(s,a)&space;&\doteq&space;\mathbb{E}[R_{t&plus;1}&space;&plus;&space;\gamma&space;q_k(S_{t&plus;1},&space;A_{t&plus;1})&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\sum_{s',r}p(s',r|s,a)[r&space;&plus;&space;\gamma&space;\sum_{a'}\pi(a'|s')q_k(s',a')]&space;\end{align*}" title="\begin{align*} q_\pi(s,a) &\doteq \mathbb{E}_\pi[G_t | S_t=s, A_t=a] \\ &= \mathbb{E}_\pi[R_{t+1} + \gamma G_{t+1} | S_t=s, A_t=a] \\ &= \mathbb{E}[R_{t+1} + \gamma v_\pi(S_{t+1}) | S_t=s, A_t=a] \\ &= \mathbb{E}[R_{t+1} + \gamma q_\pi(S_{t+1}, A_{t+1}) | S_t=s, A_t=a] \\ &= \sum_{s',r}p(s',r|s,a)[r + \gamma \sum_{a'}\pi(a'|s')q_\pi(s',a')] \\ q_{k+1}(s,a) &\doteq \mathbb{E}[R_{t+1} + \gamma q_k(S_{t+1}, A_{t+1}) | S_t=s, A_t=a] \\ &= \sum_{s',r}p(s',r|s,a)[r + \gamma \sum_{a'}\pi(a'|s')q_k(s',a')] \end{align*}" />
