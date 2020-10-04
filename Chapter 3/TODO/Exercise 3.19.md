## Exercise 3.19

### Question:

행동의 가치 ![equation](https://latex.codecogs.com/svg.latex?q_\pi(s,&space;a)) 는 바로 다음 행동에 대한 보상의 기댓값과 그 후에 이어지는 모든 보상의 기댓값을 합한 것에 따라 결정된다. 여기서도 이것을 작은 보강 다이어그램으로 생각해 볼 수 있다. 이번에는 다이어그램이 행동(상태-행동 쌍)에서 시작해서 다음 상태로 연결된다.

행동 가치 ![equation](https://latex.codecogs.com/svg.latex?q_\pi(s,&space;a)) 를 구하기 위해, 이러한 직관에 부합하는 방정식과 다이어그램을 도출하라. 이때 주어진 ![equation](https://latex.codecogs.com/svg.latex?S_t=s) 와 ![equation](https://latex.codecogs.com/svg.latex?A_t=a) 에 대해 다음 보상의 기댓값 ![equation](https://latex.codecogs.com/svg.latex?R_{t+1}) 과 다음 상태 가치의 기댓값 ![equation](https://latex.codecogs.com/svg.latex?v_\pi(S_{t+1})) 을 이용하라. 이 방정식은 기댓값을 포함해야 하는데, 이번에는 어떤 정책을 따른다는 조건 없이 계산된 기댓값이다. 다음으로 식 3.2에 정의된 ![equation](https://latex.codecogs.com/svg.latex?p(s',r|s,a)) 를 이용하여 기댓값을 분명히 표현하는 두 번째 방정식을 도출하라. 이 방정식에는 기댓값을 나타내는 표기법을 사용하지 않는다.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;q_\pi(s,a)&space;&=&space;\mathbb{E}_\pi[R_{t&plus;1}&space;&plus;&space;\gamma&space;v_\pi(S_{t&plus;1})&space;|&space;S_t=s,&space;A_t=a]&space;\\&space;&=&space;\sum_{s',r}&space;p(s',r|s,a)&space;[r&space;&plus;&space;\gamma&space;v_\pi(s')]&space;\end{align*}" title="\begin{align*} q_\pi(s,a) &= \mathbb{E}_\pi[R_{t+1} + \gamma v_\pi(S_{t+1}) | S_t=s, A_t=a] \\ &= \sum_{s',r} p(s',r|s,a) [r + \gamma v_\pi(s')] \end{align*}" />
