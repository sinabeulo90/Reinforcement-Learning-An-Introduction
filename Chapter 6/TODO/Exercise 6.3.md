## Exercise 6.3

### Question:

무작위 행보 예제의 왼쪽 그래프에서는 최초 에피소드가 오직 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;V(A)) 의 변화만 유발하는 것처럼 보인다. 이것이 첫 번째 에피소드에 어떤 일이 일어날 것인가에 대해 무엇을 말해 주는가? 왜 오직 이 한 상태에 대한 추정값만 바뀌었는가? 정확히 얼마나 바뀌었는가?

### Answer:

보상이 0이고 현재 상태의 가치 추정값과 다음 상태의 가치 추정값이 같을때, 첫 번째 에피소드에서 종단 상태를 만나기 전까지는 TD 오차 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\delta=0) 이 되므로 각 상태의 가치는 변하지 않는다.

상태 A 또는 E에서 종단 상태로 움직일 때, TD 오차 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\delta) 가 각각 -0.5, 0.5가 되므로, 상태 A와 E의 가치 추정값은 현재 추정값에서 고정 시간 간격 파라미터 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\alpha) 와 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\delta) 를 곱한 ![equation](https://latex.codecogs.com/svg.latex?\inline&space;\pm&space;(0.1&space;\times&space;0.5)) 만큼 갱신된다.