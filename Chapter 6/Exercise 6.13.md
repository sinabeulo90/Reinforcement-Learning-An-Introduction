## Exercise 6.13

### Question:

입실론 탐욕적 목표 정책을 갖는 이중 기댓값 살사의 갱신 방정식은 무엇인가?

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;Q_1(S_t,&space;A_t)&space;&\leftarrow&space;Q_1(S_t,&space;A_t)&space;&plus;&space;\alpha[R_{t&plus;1}&space;&plus;&space;\gamma&space;\mathbb{E}_\pi[Q_2(S_{t&plus;1},&space;A_{t&plus;1})&space;|&space;S_{t&plus;1}]&space;-&space;Q_1(S_t,&space;A_t)]&space;\\&space;&\leftarrow&space;Q_1(S_t,&space;A_t)&space;&plus;&space;\alpha[R_{t&plus;1}&space;&plus;&space;\gamma&space;\sum_{a}\pi(a|S_{t&plus;1})Q_2(S_{t&plus;1},&space;a)&space;-&space;Q_1(S_t,&space;A_t)]&space;\\&space;\end{align*}" title="\begin{align*} Q_1(S_t, A_t) &\leftarrow Q_1(S_t, A_t) + \alpha[R_{t+1} + \gamma \mathbb{E}_\pi[Q_2(S_{t+1}, A_{t+1}) | S_{t+1}] - Q_1(S_t, A_t)] \\ &\leftarrow Q_1(S_t, A_t) + \alpha[R_{t+1} + \gamma \sum_{a}\pi(a|S_{t+1})Q_2(S_{t+1}, a) - Q_1(S_t, A_t)] \\ \end{align*}" />

![equation](https://latex.codecogs.com/svg.latex?\inline&space;A^*&space;=&space;\text{arg}\max_a[Q_1(S,&space;a)&space;&plus;&space;Q_2(S,&space;a)]) 라고 할때,

<img src="https://latex.codecogs.com/svg.latex?\pi(a|S)&space;=&space;\begin{cases}&space;1&space;-&space;\epsilon&space;&plus;&space;\frac{\epsilon}{|A(S)|}&space;&&space;a&space;=&space;A^*&space;\\&space;\frac{\epsilon}{|A(S)}&space;&&space;a&space;\neq&space;A^*&space;\end{cases}" title="\pi(a|S) = \begin{cases} 1 - \epsilon + \frac{\epsilon}{|A(S)|} & a = A^* \\ \frac{\epsilon}{|A(S)} & a \neq A^* \end{cases}" />
