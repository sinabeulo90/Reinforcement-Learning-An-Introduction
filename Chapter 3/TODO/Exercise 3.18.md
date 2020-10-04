## Exercise 3.18

### Question:

상태의 가치는 그 상태에서 선택할 수 있는 행동의 가치와 각 행동이 현재의 정책하에서 선택될 확률이 얼마인가에 따라 결정된다. 상태로부터 시작해서 각각의 가능한 행동으로 나아가는 작은 보강 다이어그램의 측면에서 이 문제를 생각해 볼 수 있다.

시작 노드의 가치 ![equation](https://latex.codecogs.com/svg.latex?v_\pi(s)) 를 구하기 위해, 이러한 직관에 적합한 방정식과 다이어그램을 도출하라. 이때 주어진 상태 ![equation](https://latex.codecogs.com/svg.latex?S_t=s) 에 대해 각 행동 노트가 갖는 가치 ![equation](https://latex.codecogs.com/svg.latex?q_\pi(s,&space;a)) 를 이용하라. 이 방정식은 정책 ![equation](https://latex.codecogs.com/svg.latex?\pi) 를 따른다는 조건하에 계산되는 기댓값을 포함해야 한다. 다음으로 기댓값이 ![equation](https://latex.codecogs.com/svg.latex?\pi(a|s)) 로 분명히 표현되는 두 번째 방정식을 도출하라. 이 방정식에는 기댓값을 나타내는 표기법이 사용되지 않아야 한다.

### Answer:

<img src="https://latex.codecogs.com/svg.latex?\begin{align*}&space;v_\pi(s)&space;&=&space;\mathbb{E}_\pi[q_\pi(s,&space;a)]&space;\\&space;&=&space;\sum_a&space;\pi(s|a)&space;q_\pi(s,a)&space;\end{align*}" title="\begin{align*} v_\pi(s) &= \mathbb{E}_\pi[q_\pi(s, a)] \\ &= \sum_a \pi(s|a) q_\pi(s,a) \end{align*}" />
